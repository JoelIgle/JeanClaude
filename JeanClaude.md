#Codi font
```
public class JeanClaude {
    public static boolean camio(int pes){
        boolean pot = false;
        if(pes <=750 && pes >= 500){
            pot = true;
        }
        return pot;
    }

    }
```
#Test
```

import org.junit.jupiter.api.Assertions;
import org.junit.jupiter.api.Test;

public class JeanClaudeTest {

    @Test
        //Valor entre els límits
    void prova1() {
        boolean pot = JeanClaude.camio(600);
        Assertions.assertTrue(pot);
    }
    @Test //Valor superior al límit superior
    void prova2() {
        boolean pot = JeanClaude.camio(800);
        Assertions.assertFalse(pot);
    }


    @Test //Valor inferior al límit inferior
    void prova3() {
        boolean pot = JeanClaude.camio(300);
        Assertions.assertFalse(pot);
    }


    @Test
    void prova4() {
        boolean pot = JeanClaude.camio(0);
        Assertions.assertFalse(pot);
    }
    @Test
    void prova5() {
        boolean pot = JeanClaude.camio(501);
        Assertions.assertTrue(pot);
    }
    @Test
    void prova6() {
        boolean pot = JeanClaude.camio(749);
        Assertions.assertTrue(pot);
    }
    @Test
    void prova7() {
        boolean pot = JeanClaude.camio(650);
        Assertions.assertTrue(pot);
    }
    @Test
    void prova8() {
        boolean pot = JeanClaude.camio(550);
        Assertions.assertTrue(pot);
    }
    @Test
    void prova9() {
        boolean pot = JeanClaude.camio(10000);
        Assertions.assertFalse(pot);
    }
    @Test //Valor no és un número
    void prova10 () {
        boolean pot = JeanClaude.camio(Integer.parseInt("dos"));
        Assertions.assertFalse(pot);
    }
    
}
```
