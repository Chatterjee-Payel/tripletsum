# tripletsum
 public:
    //Function to find if there exists a triplet in the 
    //array A[] which sums up to X.
    bool find3Numbers(int A[], int n, int X)
    {
        //Your Code Here
        sort(A,A+n);
        for(int i=0;i<n-2;i++){
            int lo=i+1;
            int hi=n-1;
            int sum=X-A[i];
            while(lo<hi)
            {
                if(A[lo]+A[hi]==sum)
                {
                    return true;
                }
                else if(A[lo]+A[hi]<sum){
                 lo++;
                 }
                 else 
                 hi--;
            }
        }
        return false;
    }
};
