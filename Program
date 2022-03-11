import java.io.FileInputStream;
import java.io.IOException;
import java.util.*;

public class Wordcounter {
	
	public static HashMap<String,Integer> sortByValue (HashMap<String, Integer> hm)
	{
		List<Map.Entry<String, Integer>>list= new LinkedList<Map.Entry<String,Integer>>(hm.entrySet());
		
		Collections.sort(list, new Comparator<Map.Entry<String,Integer>>(){
			
			public int compare(Map.Entry<String, Integer> o1,Map.Entry<String,Integer>o2)
			{
				return (o1.getValue()).compareTo(o2.getValue());
			}
			
		});
		
		HashMap<String, Integer>temp=new LinkedHashMap<String,Integer>();
		for(Map.Entry<String,Integer>aa:list) {
			temp.put(aa.getKey(),aa.getValue());
		}
		
		return temp;
	}
	

	public static void main(String[] args) throws IOException{
		
		FileInputStream fin = new FileInputStream("Data");
		Scanner fileInput = new Scanner(fin);
		
		ArrayList<String> words = new ArrayList<String>();
		ArrayList<Integer> count = new ArrayList<Integer>();
		
		while(fileInput.hasNext()) {
			
			String nextWord = fileInput.next();
			if(words.contains(nextWord))
			{
				int index = words.indexOf(nextWord);
				count.set(index,  count.get(index) +1);
			}
			else
			{
				words.add(nextWord);
				count.add(1);
			}
			
		}
		
		fileInput.close();
		fin.close();
		
		HashMap<String,Integer> hm = new HashMap<String,Integer>();
		
		for(int i=0;i<count.size();i++) 
		{
			hm.put(words.get(i),count.get(i));
		}
		
		Map<String,Integer> hm1 = sortByValue(hm);
		
		ArrayList arr = new ArrayList();
		ArrayList arr1 = new ArrayList();
		Set<Map.Entry<String,Integer>>se=hm1.entrySet();
		
		for(Map.Entry<String,Integer> se1:se) 
		{
			arr.add(se1.getKey());
			arr1.add(se1.getValue());
		}
		
		for(int i=arr.size()-1;i>=arr.size()-10;i--) 
		{
			System.out.println(arr.get(i)+" "+arr1.get(i));
		}

	}

}
