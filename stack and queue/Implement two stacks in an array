class twoStacks {
  public:
        int a[10001];
        int top1;
        int top2;
      twoStacks() {
       top1=-1;
       top2=10001;    
      }

    // Function to push an integer into the stack1.
    void push1(int x) {
        if(top1<top2-1)
            a[++top1]=x;
        return;
        
    }

    // Function to push an integer into the stack2.
    void push2(int x) {
        if(top2>top1+1){
            a[--top2]=x;
        }
        return;
    }

    // Function to remove an element from top of the stack1.
    int pop1() {
        if(top1==-1)
            return(-1);
        return(a[top1--]);
        
    }

    // Function to remove an element from top of the stack2.
    int pop2() {
        if(top2==10001)
            return(-1);
        return(a[top2++]);
        
    }
};
