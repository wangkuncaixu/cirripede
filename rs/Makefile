OPENSSL_DIR=/home/me/.local/openssl

all: rs

rs: rs.cc curve25519-20050915/curve25519.a curve25519-20050915/curve25519.h
	g++ -g -Wall -lboost_thread -lpcap -I${OPENSSL_DIR}/include -o rs rs.cc curve25519-20050915/curve25519.a ${OPENSSL_DIR}/lib/libcrypto.a ${OPENSSL_DIR}/lib/libssl.a && rm -f curve25519-20050915/curve25519.h curve25519-20050915/x86cpuid.out curve25519-20050915/curve25519.impl curve25519-20050915/curve25519.impl.check curve25519-20050915/x86cpuid curve25519-20050915/curve25519.impl.check.h curve25519-20050915/test-curve25519

curve25519-20050915/curve25519.h:
	(cd curve25519-20050915 && make)

curve25519-20050915/curve25519.a:
	(cd curve25519-20050915 && make)

clean:
	rm -f rs *~ curve25519-20050915/curve25519.h curve25519-20050915/x86cpuid.out curve25519-20050915/curve25519.impl curve25519-20050915/curve25519.impl.check curve25519-20050915/x86cpuid curve25519-20050915/curve25519.impl.check.h curve25519-20050915/test-curve25519