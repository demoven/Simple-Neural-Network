import math
import numpy as np 

#inputs
ex1 = [1,0,0]
ex2 = [1,0,1]
ex3 = [1,1,0]
ex4 = [1,1,1]
ex1yd = 0
ex2yd = 0
ex3yd = 0
ex4yd = 1

#weights
w = [np.random.rand(), np.random.rand(), np.random.rand()] #random 0-1

#learning rate
a=1

def degrau(x):
		return 1 if x >= 0 else 0
    
def erro(yd, y):
	return yd-y
  
#change weights
def mudarPesos(w,e,x):
    i=0
    while i<len(w):
    	w[i]=w[i]+a*e*x[i]
        i+=1
    return w

#sum function
def somatorio(x,w):
    i=0
    soma = 0
    while i<len(x):
        soma+=x[i]*w[i]
        i+=1
    return soma

#neuron
def neuronio(x,w):
    soma = somatorio(x,w)
    #input
    y=-1
    y = degrau(soma)
    
    return y

#NN train
def treinarRede(ex1,ex2,ex3,ex4,w):
    saida = neuronio(ex1,w)
    erro1 = erro(ex1yd,saida)
    if(erro1!=0):
        w = mudarPesos(w,erro1,ex1)
    saida = neuronio(ex2,w)
    erro2 = erro(ex2yd,saida)
    if(erro2!=0):
         mudarPesos(w,erro2,ex2)
    saida = neuronio(ex3,w)
    erro3 = erro(ex3yd,saida)
    if(erro3!=0):
    	w = mudarPesos(w,erro3,ex3)
    saida = neuronio(ex4,w)
    erro4 = erro(ex4yd,saida)
    if(erro4!=0):
        mudarPesos(w,erro4,ex4)

    erroTotal=pow(erro1, 2)+ pow(erro2, 2) + pow(erro3, 2) + pow(erro4, 2)
    return erroTotal

#error
erroCalc = 99999999
numIt = 0

#main loop to train
while erroCalc > 0.01:
	erroCalc = treinarRede(ex1,ex2,ex3,ex4,w)
	numIt+=1

#test data
xTeste = [1,0,1]
xTeste2 = [1,1,1]
xTeste3 = [1,0,1]
xTeste4 = [1,1,1]
xTeste5 = [1,0,0]
xTeste6 = [1,1,0]
xTeste7 = [1,1,1]

y = neuronio(xTeste,w)
print "Primeiro teste:", y
y = neuronio(xTeste2,w)
print "Segundo teste:",y
y = neuronio(xTeste3,w)
print "Terceiro teste:",y
y = neuronio(xTeste4,w)
print "Quarto teste:",y 
y = neuronio(xTeste5,w)
print "Quinto teste:",y
y = neuronio(xTeste6,w)
print "Sexto teste:",y 
y = neuronio(xTeste7,w)
print "Setimo teste:",y
