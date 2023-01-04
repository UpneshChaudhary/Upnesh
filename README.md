# Upnesh
int Solution::solve(vector<int> &A, int B) {
    int max_sum = INT_MIN;
    int sum =0;
    for(int i =0; i<B; i++){
        sum+=A[i];
        max_sum = sum;
    }
    int r = A.size()-1;
    for(int i=B-1; i>=0; i--){
        sum-=A[i];
        sum+=A[r];
        max_sum = max(max_sum, sum);
        r--;
    }
    return max_sum;
}
