CXX = g++

CFLAGS = -std=c++11 -g -pedantic -Wall -Werror

OBJS = cmd_parse_unitest.o dbg_probability_wrapper.o

TARGETS = cmd_parse_unitest

$(TARGETS): $(OBJS)
	$(CXX) -o $@ $(OBJS)

cmd_parse_unitest.o: cmd_parse_unitest.cpp ../utils.h ../probability_wrapper.h ../error_flag.h
	$(CXX) -c $< $(CFLAGS) -DDEBUG

dbg_probability_wrapper.o: ../probability_wrapper.cpp ../probability_wrapper.h
	$(CXX) -c $< $(CFLAGS) -o $@ -DDEBUG

.PHONY: clean
clean:
	rm $(OBJS) $(TARGETS)