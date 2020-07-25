import math

px=-0.27
py=9.37
pz=7.10

t0=0
t1=0
t2=0
t3=0
t4=0
t5=0

x=0  #roll  

y=0  #pitch 

z=0  #yaw 

def Euler_Inverse(Px,Py,Pz,x,y,z):

    global pz,py,px,t0,ti0,t1,ti1,t2,ti2,t3,ti3,t4,ti4,t5,ti5
    L0_1=7
    L1_2=26.5
    L2_3=27.3
    L3_4=32
   
	
    r=math.sqrt(pow(px,2)+pow(py,2))
    
    alpha=math.atan2((pz-L0_1),r)
    Omega=math.atan2(L2_3*math.sin(t2),L1_2+L2_3*math.cos(t2))
    D=-(pow(px,2)+pow(py,2)+pow(pz-L0_1,2)-pow(L1_2,2)-pow(L2_3,2))/(2*L1_2*L2_3)

    t0=math.atan2(px,py)+z+2.37

    #t0=math.atan2(px,py)
      
    
    t2=math.atan2(math.sqrt(1-pow(D,2)),D)+px/4	    
	
    #t2=math.atan2(math.sqrt(1-pow(D,2)),D)

    t1=alpha-Omega

    #alpha_1=z-t0
    #beta_1=y-(t1+t2)

    #d4rx=L3_4*math.cos(beta_1)*math.sin(alpha_1)

    #d4rz=L3_4*math.sin(beta_1)

    #t3=math.atan2(d4rx,d4rz)

    #t4=math.atan2(math.sqrt(pow(d4rx,2)+pow(d4rz,2)),math.cos(beta_1)*math.cos(alpha_1))

    #t5=x-t3



    u=-math.cos(t0)*(math.cos(z)*math.sin(x)-math.cos(x)*math.sin(y)*math.sin(z))-math.sin(t0)*(math.sin(x)*math.sin(z)+math.cos(x)*math.cos(z)*math.sin(y))

    v=math.cos(x)*math.cos(y)*math.sin(t1+t2)+math.cos(t0)*math.cos(t1+t2)*(math.sin(x)*math.sin(z)+math.cos(x)*math.cos(z)*math.sin(y))-math.sin(t0)*math.cos(t1+t2)*(math.cos(z)*math.sin(x)-math.cos(x)*math.sin(y))

    t3=math.atan2(u,v)
		
    k=-math.sin(y)*math.cos(t1+t2)-math.cos(t0)*math.cos(y)*math.cos(z)*math.sin(t1+t2)-math.cos(y)*math.sin(t0)*math.sin(z)*math.sin(t1+t2)
	    

    m=math.cos(y)*math.sin(x)*math.cos(t1+t2)+math.cos(t0)*math.sin(t1+t2)*(math.cos(x)*math.sin(z)-math.cos(z)*math.sin(x)*math.sin(y))-math.sin(t0)*math.sin(t1+t2)*(math.cos(x)*math.cos(z)+math.sin(x)*math.sin(y)*math.sin(z))	    

		    
    e=math.cos(x)*math.cos(y)*math.cos(t1+t2)-math.cos(t0)*math.sin(t1+t2)*(math.sin(x)*math.sin(z)+math.cos(x)*math.cos(z)*math.sin(y))+math.sin(t0)*math.sin(t1+t2)*(math.cos(z)*math.sin(x)-math.cos(x)*math.sin(y)*math.sin(z))

	   
    t4=math.atan2(e,math.sqrt((1-pow(e,2))))

    t5=math.atan2(k,m)

    #f=math.cos(t0)*(math.cos(x)*math.cos(z)+math.sin(x)*math.sin(y)*math.sin(z))+math.sin(t0)*(math.cos(x)*math.sin(z)-math.cos(z)*math.sin(x)*math.sin(y))

    #t5=math.asin((-f))-t3

    #t5=math.atan2(-f,math.sqrt((1-pow(f,2))))

    return "t0:",t0,"t1:",t1,"t2:",t2,"t3:",t3,"t4:",t4,"t5:",t5

Angles=Euler_Inverse(0.2,0.4,0.7,0.1,0.2,0.4)   # input values : location of end effector px py pz  and  roll , pitch yaw angles of end effector x y z

print(Angles)	


    
