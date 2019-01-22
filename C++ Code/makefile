CFLAGS_COMMON = -Wall -O3 -static
LDFLAGS_COMMON = 

# Use "g++" to compile source files
CC_GCC = g++
# Use "g++" to link object files
LD_GCC = g++
# Compiler flags
CFLAGS_GCC = -Wall -O3 -static $(CFLAGS_COMMON)
# Linker flags
LDFLAGS_GCC = -w -O3 $(LDFLAGS_COMMON)

MAINOBJS = OptimizedPitRemoval.o

EXE_GCC=OptimizedPitRemoval_gcc

# Linkage rule EXE_GCC
$(EXE_GCC).exe: $(MAINOBJS:%.o=obj/$(EXE_GCC)/%.o)
	$(LD_GCC) $(LDFLAGS_GCC) $(MAINOBJS:%.o=obj/$(EXE_GCC)/%.o) -o $(EXE_GCC).exe

# Compile main object files
$(MAINOBJS:%.o=obj/$(EXE_GCC)/%.o): obj/$(EXE_GCC)/%.o: %.cpp *.h
	$(MD) -p obj/$(EXE_GCC)
	$(CC_GCC) $(CFLAGS_GCC) -c $< -o $@