# Simulation-voiture
Pour notre application on a utilisé la notion des threads pour gérer simultanément  les feux, le déplacement des véhicules et le traçage  dans la fenêtre graphique. Pour cela les classes Feu et Véhicules ont hérité à partir de la classe Thread, et en redéfinissant la méthode run()  on a  affecter a chaque thread son fonctionnement :

Classe Feu :
public void run()
 {
       while(true)
       {
       try {
             sleep(5000);
       } catch (InterruptedException e) {
             e.printStackTrace();
       }
       if(clr==Color.red)
             clr=Color.green;
       else
             clr=Color.red;
       try {
             sleep(5000);
       } catch (InterruptedException e) {
             e.printStackTrace();
       }
       if(clr==Color.red)
             clr=Color.green;
       else
             clr=Color.red;
            
       }
       }
Classe Vehicule :
public void run()
 {
        while(true)
        {
       try {
             sleep(100);
       } catch (InterruptedException e) {
             // TODO Auto-generated catch block
             e.printStackTrace();
       }
if(isRoule())
        move();
        }
 }
