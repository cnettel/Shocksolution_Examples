# location of the Python header files
 
 
PYTHON_VERSION=2.7
PYTHON_INCLUDE=-I/sw/comp/python/2.7.6_tintin/include/python2.7 -I/sw/comp/python/2.7.6_tintin/include/python2.7
# location of the Boost Python include files and library
 
BOOST_INC = $(BOOST_ROOT)/bin
BOOST_LIB = $(BOOST_ROOT)/lib
 
# compile mesh classes
TARGET = hello_ext
 
$(TARGET).so: $(TARGET).o
	g++ -shared -Wl,--export-dynamic $(TARGET).o -lboost_python -lpthread -ldl -lutil -lm -lpython2.7 -Xlinker -export-dynamic -o $(TARGET).so
 
$(TARGET).o: $(TARGET).cpp
	g++ -I$(PYTHON_INCLUDE) -fPIC -c $(TARGET).cpp
