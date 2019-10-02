//author Guillem Ardanuy Martinez

import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;
import java.util.Comparator;

public class Main {

    public static void main(String[] args) {
        // write your code here
        //creem array de numeros
        // creem llista de digits ocurreguts
        //creem auxiliar de llista de digits de cada numero
        //si el tamany del numero es igual al tamañ de la llista de digits de cada numero, significa que es mante, en la llista de numeros,
        //i els valors de digits auxiliars, s'afegeixen a la llista de digits ocurreguts, sino no
        ArrayList llistaNumeros= new ArrayList();
        llistaNumeros.add(10);
        llistaNumeros.add(23);
        llistaNumeros.add(45);
        llistaNumeros.add(56);
        llistaNumeros.add(1888);
        llistaNumeros.add(9779);
        llistaNumeros.add(999);
        llistaNumeros.add(88088);
        llistaNumeros.add(777);
        llistaNumeros.add(88888);

        ArrayList llistaDigitsOcurreguts= new ArrayList();
        ArrayList llistaAuxiliarDigitsCadaNumero= new ArrayList();

        System.out.println("lista original --> "+llistaNumeros);

        Collections.sort(llistaNumeros);  // ordenem per asegurar que recorrerem de gran a petit, per fer-ho comensarem desde el ultim i anirem fins al primer
        System.out.println("llista ordenada --> "+llistaNumeros);
       Collections.sort(llistaNumeros,Collections.reverseOrder());
        System.out.println("reverse list --> "+llistaNumeros);


        int indexNumeros=1;//comencerem a recorrer la llista de numeros per el segon element, ja que el primer sempre afegirem els digits a digits ocurreguts
        for(int indexInicial=0;indexInicial<llistaNumeros.get(0).toString().length();indexInicial++){
            llistaDigitsOcurreguts.add(llistaNumeros.get(0).toString().charAt(indexInicial)); //afegim els digits del primer numero a llistaDIgitsOcurreguts
        }

        while (indexNumeros<llistaNumeros.size()){
            String numero=llistaNumeros.get(indexNumeros).toString();
            int indexDigits=0;
            int contadorAuxiliar=0;
            while(indexDigits<numero.length()){ // recorrem digit a digit
                char digit=numero.charAt(indexDigits);
                if(!llistaDigitsOcurreguts.contains(digit)){
                    llistaAuxiliarDigitsCadaNumero.add(digit);
                    contadorAuxiliar++;
                }
                indexDigits++;
            }//fi while digit a digit
            if(contadorAuxiliar==numero.length()){
                //System.out.println("el numero que te igual tamany que contador auxiliar es: "+numero);
                contadorAuxiliar=0;
                for(int j=0;j<llistaAuxiliarDigitsCadaNumero.size();j++){
                    //  System.out.println("afegir al auxiliar --> "+llistaAuxiliarDigitsCadaNumero.get(j)+" ... "+llistaAuxiliarDigitsCadaNumero);
                    llistaDigitsOcurreguts.add(llistaAuxiliarDigitsCadaNumero.get(j));
                }


            }
            else{
                //System.out.println("numero que descartem "+ numero+" que en la llista detecta que es: "+llistaNumeros.get(indexNumeros));
                llistaNumeros.remove(indexNumeros);
                llistaAuxiliarDigitsCadaNumero.clear();
                // System.out.println("llistaAUxiliar despres de buidar es : "+ llistaAuxiliarDigitsCadaNumero);
                indexNumeros--;
            }
            indexNumeros++;

        }//fi recorrer numers de la llista
        //System.out.println("la llista ara es : -> "+ llistaNumeros);

        int sumaTotal=0;
        for(int k=0;k< llistaNumeros.size();k++){
            sumaTotal+=Integer.parseInt(llistaNumeros.get(k).toString());
        }

        Collections.sort(llistaNumeros);

        System.out.println("llista: "+llistaNumeros+" SUMA ES: " +sumaTotal);
    }// fi psvm
}// fi main
