we are given two arrays that represent the arrival and depature time of train,The task is to find the minimum no of the platforms required.But train should not wait 

arr[] = {9:00,9:40,9:50,11:00,15:00,18:00}
dep[]={9:10,12:00,11:20,11:30,19:00,20:00}


output : minimum platforms needed : 3 
#problem-solving-train-code
class Main {
    public static void main(String[] args) {
        
        int[] ar={900,940,950,1100,1500,1800};
        int[] dep = {910,1200,1120,1130,1900,2000};
        int n = 6;
        int count =0;
        int pltfm =0;
        for(int i=0,j=0;i<n && j<n;){
            if(ar[i]<dep[j]){
                count++;
                pltfm=Math.max(pltfm,count);
                i++;
            }else{
                count--;
                j++;
            }
        }
        System.out.println(pltfm);
    }
}
