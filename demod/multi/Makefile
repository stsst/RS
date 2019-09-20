CC:=gcc
LD:=gcc
CFLAGS:=-O2
LDFLAGS:=
PROG:=multi
OBJS:=rs_multi.o demod_base.o bch_ecc_mod.o rs41base.o dfm09base.o m10base.o lms6Xbase.o
LIBS:=-lm -lpthread
HEADERS:=$(wildcard *.h)

.PHONY: all
all: $(PROG)

%.o: %.c $(HEADERS)
	$(CC) $(CFLAGS) -c $< -o $@

$(PROG): $(OBJS)
	$(LD) $(LDFLAGS) -o $@ $^ $(LIBS)

.PHONY: clean
clean:
	rm -f $(PROG) $(OBJS)

