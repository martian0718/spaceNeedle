# spaceNeedle
Spaceneedle Project
public class SpaceNeedle
{
    public static final int Size=4;
   public static String hash = "";
   public static void main(String[] args){
        needle(Size);
        top(Size);
        middle(Size);
        bottom(Size);
        needle(Size);
        doubleNeedle(Size);
        top(Size);
        middle(Size);
        System.out.println(hash);
        System.out.print(hash.hashCode());      
    }
   public static void needle(int input){
        for(int row=1;row<=Size;row++){
            for(int space=1;space<=(3*Size);space++){
                hash+=" ";
            }
            hash+="||";
            hash+="\n";
        }
    }
    public static void roof(int input){
        for(int space=1;space<=(3*Size-3);space++){
                hash+=" ";
         }               
        hash+="__/||\\__";        
        hash+="\n";
   }
   public static void top(int input){
        for(int row=1;row<=Size;row++){
            for(int space=1;space<=(3*Size-3*row);space++){                    
                hash+=" ";
            }            
            hash+="__/";
            for(int colon=1;colon<=((row-1)*3);colon++){                
                hash+=":";
            }            
            hash+="||";
            for(int colon=1;colon<=((row-1)*3);colon++){                
                hash+=":";
            }           
            hash+="\\__";            
            hash+="\n";
        }
    }
   public static void middle(int input){        
        hash+="|";
        for(int quote=1;quote<=(Size*6);quote++){            
            hash+="\"";
        }        
        hash+="|";        
        hash+="\n";
    }
   public static void bottom(int input){
       for(int row=1;row<=Size;row++){
           for(int space=1;space<=(2*row-2);space++){               
               hash+=" ";
            }           
           hash+="\\_";
           for(int ups=1;ups<=(3*Size+1-2*row);ups++){               
               hash+="/\\";
                }           
           hash+="_/";           
           hash+="\n";
        }
    }
   public static void doubleNeedle(int input){
        for(int row=1;row<=(Size*Size);row++){
            for(int space=1;space<=(Size*2+1);space++){                
                hash+=" ";
            }            
            hash+="|";
            for(int percent=1;percent<=(Size-2);percent++){                
                hash+="%";
            }
            hash+="||";
            for(int percent=1;percent<=(Size-2);percent++){
                hash+="%";
            }
            hash+="|";            
            hash+="\n";
        }   
    }
}
