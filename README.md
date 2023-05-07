# UFx
 UFX is a pure Python library that implements a disjoint set data structure that allows for federated lookup operations. 

 Two implementation schemes have been proposed. Java content 

 uf_ Hash using Python dictionary 
 uf_ Tree uses nodes linked to each anstror 
 These implementations are designed for hash types. Regardless, you can use the UFNode class $that exists in ^ {tt2} to implement non hash types (see the API documentation section below). 

 UFX is only tested with Python 2.7, Python 3.5, and Python, but other versions of Python virtual machines may be used. 

 performance 
 uf_ The hash implementation is recommended. It performs well using the classic Python virtual machine. uf_ Tree implementation is slow because Python's pointer performance is poor based on data structures. Using another Python virtual machine is recommended_ Use it when implementing a tree. 

 Todo: Calculation speed and memory consumption table 

 API documentation 
 Import 
 An implementation structure for importing disjoint set data 

 from ufx import uf_ tree as ufx 
 or 

 from ufx import uf_ hash as ufx 
 Quick examples 
 import sys 
 import random 
 uf = ufx.UnionFind() 
 az = "abcdefghijklmnopqrstuvwxyz" 
 az += az.upper() 
 for e in az: 
 uf.make_ set(e) 
 i = 0 
 while i < 26: 
 i += 1 
 uf.union(random.choice(az), random.choice(az)) 
 print(uf) 
 print(uf.get_size('a')) 
 uf.clear() 
 print(uf) 
 Hash type 
 To-do list 

 Non hash type 
 Take a look at this class UFNode 
