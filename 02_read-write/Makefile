.PHONY: clean

CFLAGS  := -Wall -Werror -g
LD      := gcc
LDFLAGS := ${LDFLAGS} -lrdmacm -libverbs -lpthread

APPS    := rdma-client rdma-server

all: ${APPS}

rdma-client: rdma-common.o rdma-client.o
	${LD} -o $@ $^ ${LDFLAGS}

rdma-server: rdma-common.o rdma-server.o
	${LD} -o $@ $^ ${LDFLAGS}

clean:
	rm -f *.o ${APPS}

