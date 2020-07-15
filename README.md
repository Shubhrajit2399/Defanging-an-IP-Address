# Defanging-an-IP-Address

class Solution {
    public String defangIPaddr(String address) {
        String[] a=address.split("");
        String[] a1=new String[address.length()];
        StringBuffer sb = new StringBuffer();
        String s;
        for(int i=0;i<a.length;i++){
            if(a[i].equals(".")){
                a1[i]="["+a[i]+"]";
            }
            else{
                a1[i]=a[i];
            }
        }
        for(int i=0;i<a1.length;i++){
            sb.append(a1[i]);
        }
        s=sb.toString();
        return s;
    }
}
