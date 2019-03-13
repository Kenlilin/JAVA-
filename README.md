# JAVA-
日常学习的Java的一些基础题目
运用选择排序，按学生的成绩进行排名
public class P238_17 {
	public static void main(String[] args) {
		String [] m = {"a","b","c"};
		double [] n = {85,92,60};
		Selection(m,n);
	}
	public static void Selection(String [] m,double [] n){
		for(int i = 0;i<n.length-1;i++){
			double max = n[i];
			int maxIndex = i;
			String sMax = m[i];
			int sMaxIndex = i;
			for(int j = i+1;j<n.length;j++){
				if(max<n[j]){
					max = n[j];
					maxIndex = j;
					sMax = m[j];
					sMaxIndex = j;
				}
			}
			if(maxIndex!=i){
				n[maxIndex] = n[i];
				n[i] = max;
				m[sMaxIndex] = m[i];
				m[i] = sMax;
			}
		}
		System.out.println(java.util.Arrays.toString(m)+"  "+java.util.Arrays.toString(n));
	}
