# bitwise
class bitwise implemented


//----------------------------------------------class java 
public class Cbitwise {
    int x; 
    public Cbitwise(){
        this.x = 0 ;
    }

    public void Set1 (int pos){
        int mask=1; 
        mask = mask << pos-1; 
        x = x | mask; 
    }

    public void Set0(int pos ){
        int mask = 1 ; 
        mask = mask<<pos-1; 
        mask = ~mask; 
        x=x&mask; 
    }

    public int Getbit(int pos){
        int mask= 1; 
        mask = mask<<pos-1; 
        mask=x&mask; 
        mask= mask>>>pos-1; 
        return mask; 
    }
}
