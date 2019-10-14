# NUMPYfunctions
numpy fxnx
class cumpy:
    def __init__(self,a):
        self.a=a
    def ndim(self):
        arr=self.a
        if isinstance(arr[0],int):
            print("1-D")
        else:
            print("2-D")
            
    def shape(self):
        arr=self.a
        row=len(arr)
        if isinstance(arr[0],int):
            print("1*{}".format(row))
        else:
            column=len(arr[0])
            print("{0}*{1}".format(row,column))
    
    def reval(self):
        arr=self.a
        list=[]
        row=len(arr)
        col=len(arr[0])
        for i in range(0,row):
            for j in range(0,col):
                list.append(arr[i][j])
        return(list)
    
    def reshape(self,r,c):
        array=self.a
        arr=cumpy.reval(self)
        l=[]
        d=0
        for i in range(0,r):
            k=[]
            for j in range(0,c):
                k.append(arr[d])
                d+=1
            l.append(k)
        return(l)
    
def main():
    arr=[1,2,3,4,5,6]
    array=[[1,2],[3,4],[5,6]]
    p=cumpy(arr)
    o=cumpy(array)
    print(o.reval())
    print(o.reshape(3,2))
    p.shape()
    o.shape()
    
    
if __name__=="__main__":
    main()
        
            
