# Animal-Guessing-Game
This is a program where the user has to pick from a list of 20 animals. Once this is done the computer will ask questions in an attempt to guess the users animal!


import java.util.Scanner;
import java.util.*;

class Animal
{
    private String animalName;
    private boolean isWet;
    private boolean isFurry;
    private boolean hasWings;
    private boolean isWarmBlooded;
    private boolean laysEggs;
    private boolean isCarnivorous;
    private boolean isColorful;
    //isColorful refers to the main colors of the animal. If colors include white, grey, black, or brown, those are considered UNCOLORFUL(FALSE) while any other color(green, red, purple, yellow etc) would be considered colorful(TRUE)
    private String imageLink;

    public Animal(String animalName, boolean isWet, boolean isFurry, boolean hasWings, boolean isWarmBlooded, boolean laysEggs, boolean isCarnivorous, boolean isColorful, String imageLink)
    {
        this.animalName = animalName;
        this.isWet = isWet;
        this.isFurry = isFurry;
        this.hasWings = hasWings;
        this.isWarmBlooded = isWarmBlooded;
        this.laysEggs = laysEggs;
        this.isCarnivorous = isCarnivorous;
        this.isColorful = isColorful;
        this.imageLink = imageLink;
    }
    
    public String toString()
    {
        String result = animalName + " is an animal that: ";
        if (isWet){
            result = result + "likes the water, ";
        }
        else{
            result = result + "likes the land, ";
        }
        
        if (isFurry){
            result = result + "has fur, ";
        }
        else {
            result = result + "does not have fur, ";
        }
        
        if (hasWings){
            result = result + "can fly, ";
        }
        else {
            result = result + "cannot fly, ";
        }
        
        if (isWarmBlooded){
            result = result + "is warm blooded, ";
        }
        else{
            result = result + "is cold blooded, ";
        }
        
        if (laysEggs){
            result = result + "can lay eggs, ";
        }
        else {
            result = result + "has live birth, ";
        }
        if (isCarnivorous){
            result = result + "is a carnivorous species, ";
        }
        else {
            result = result + "is either an omnivorous or herbivorous species, ";
        }
        if(isColorful){
            result = result + "has at least one color in the rainbow";
        }
        else {
            result = result + "has nuetral color tones";
        }
        
        return result;
    }
    
    public String getType()
    {
        return "Undefined";
    }
    
    public boolean getIsWet()
    {
        return isWet;
    }
    
    public boolean getIsFurry()
    {
        return isFurry;
    }
    
    public boolean getHasWings()
    {
        return hasWings;
    }
    
    public boolean getIsWarmBlooded()
    {
        return isWarmBlooded;
    }
    
    public boolean getLaysEggs()
    {
        return laysEggs;
    }
    
    public boolean getIsCarnivorous()
    {
        return isCarnivorous;
    }
    
    public boolean getIsColorful()
    {
        return isColorful;
    }
    
    public String getAnimalName()
    {
        return animalName;
    }
    
    public String getImageLink()
    {
        return "If you are interested here is a link to an image to view your chosen animal: \n" + imageLink;
    }
}

class Mammal extends Animal
{
    
    public Mammal(String mammalName, boolean isWet, boolean isFurry, boolean hasWings, boolean isWarmBlooded, boolean laysEggs, boolean isCarnivorous, boolean isColorful, String imageLink)
    {
        super(mammalName, isWet, isFurry, hasWings, isWarmBlooded, laysEggs, isCarnivorous, isColorful, imageLink);
    }
    
    public String toString()
    {
        String result = super.toString();
        result = result + ", and is a mammal!"; 
        return result;
    }
    
     public String getMammalName()
    {
        return super.getAnimalName();
    }
    
    public String getType()
    {
        return "Mammal";
    }
}

class Bird extends Animal
{
    
    public Bird(String birdName, boolean isWet, boolean isFurry, boolean hasWings, boolean isWarmBlooded, boolean laysEggs, boolean isCarnivorous, boolean isColorful, String imageLink)
    {
       super(birdName, isWet, isFurry, hasWings, isWarmBlooded, laysEggs, isCarnivorous, isColorful, imageLink);
    }
    
    public String toString()
    {
        String result = super.toString();
        result = result + ", and is a bird!";
        return result;
    }
    
    public String getBirdName()
    {
        return super.getAnimalName();
    }
    
    public String getType()
    {
        return "Bird";
    }
    
}

class Fish extends Animal
{
    
    public Fish(String fishName, boolean isWet, boolean isFurry, boolean hasWings, boolean isWarmBlooded, boolean laysEggs, boolean isCarnivorous, boolean isColorful, String imageLink)
    {
       super(fishName, isWet, isFurry, hasWings, isWarmBlooded, laysEggs, isCarnivorous, isColorful, imageLink);
    }
    
    public String toString()
    {
        String result = super.toString();
        result = result + ", and is a fish!";
        return result;
    }
    
    public String getFishName()
    {
        return super.getAnimalName();
    }
    
    public String getType()
    {
        return "Fish";
    }
}

class Reptile extends Animal
{
    
    public Reptile(String reptileName, boolean isWet, boolean isFurry, boolean hasWings, boolean isWarmBlooded, boolean laysEggs, boolean isCarnivorous, boolean isColorful, String imageLink)
    {
     super(reptileName, isWet, isFurry, hasWings, isWarmBlooded, laysEggs, isCarnivorous, isColorful, imageLink);
    }
    
    public String toString()
    {
        String result = super.toString();
        result = result + ", and is a reptile!";
        return result;
    }
    
    public String getReptileName()
    {
        return super.getAnimalName();
    }
    
    public String getType()
    {
        return "Reptile";
    }
}

class Amphibian extends Animal
{
    
    public Amphibian(String amphibianName, boolean isWet, boolean isFurry, boolean hasWings, boolean isWarmBlooded, boolean laysEggs, boolean isCarnivorous, boolean isColorful, String imageLink)
    {
        super(amphibianName, isWet, isFurry, hasWings, isWarmBlooded, laysEggs, isCarnivorous, isColorful, imageLink);
    }
    
    public String toString()
    {
        String result = super.toString();
        result = result + ", and is an amphibian!";
        return result;
    }
    
    public String getAmphibianName()
    {
        return super.getAnimalName();
    }
    
    public String getType()
    {
        return "Amphibian";
    }
}


class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        
        ArrayList<Animal> animal = new ArrayList<Animal>();
        animal.add(new Mammal ("Bat", false, true, true, true, false, false, false, "https://www.batcon.org/wp-content/uploads/2024/05/Grey-headed-flying-foxVivian-Jones.jpg"));
        animal.add(new Mammal ("Camel", false, true, false, true, false, false, true, "https://www.clevelandzoosociety.org/files/blog/featured/adobestock50535217.jpg "));
        animal.add(new Mammal ("Fox", false, true, false, true, false, true, true, "https://visitclearcreek.com/wp-content/uploads/2020/07/wildlife_fox_clear_creek_county.jpg "));
        animal.add(new Mammal ("Leopard", false, true, false, true, false, true, true, "https://images.squarespace-cdn.com/content/v1/66ec3b49803ab81bf84f89e4/1737488319255-I9Y2KQ7FG8NLIZ15TZS0/Reno-Leopard-2025.jpg"));
        animal.add(new Mammal ("Pangolin", false, false, false, true, false, true, false, "https://cdn.conscious-explorer.com/keycdn/file/11ac575d48abebd8f7bc49ac4f5c16c5286bd2ed9c09d80c81af9ad8254452b4/QhtKnF54KofP6oDE.webp"));
        animal.add(new Mammal ("Platypus", true, true, false, true, true, true, false, "https://museumsvictoria.com.au/media/16781/platypus-closeup.jpg"));
        animal.add(new Mammal ("Sea Otter", true, true, false, true, false, true, false, "https://i.natgeofe.com/n/7251299a-3dcf-4634-9b03-d6079078174c/OG_Sea-Otter_Protecting-Sealife_FAMILY_0522.jpg"));
        animal.add(new Mammal ("Walrus", true, false, false, true, false, true, false, "https://www.randomlists.com/img/animals/walrus.webp"));
        animal.add(new Mammal ("Whale", true, false, false, true, false, true, false, "https://cdn.mos.cms.futurecdn.net/zW4aUdwaTRhoiwGGjN4qeN-1200-80.jpg"));
        
        animal.add(new Bird ("American Kestrel", false, false, true, true, true, true, true, "https://www.allaboutbirds.org/guide/assets/photo/302366931-480px.jpg"));
        animal.add(new Bird ("Common Loon", true, false, true, true, true, true, false, "https://media.audubon.org/nas_birdapi_hero/a1_4357_1_common_loon_sunil_gopalan_kk_breeding_adult_and_downy_young.jpg?height=944&auto=webp&quality=90&fit=bounds&disable=upscale"));
        animal.add(new Bird ("Great Blue Heron", true, false, true, true, true, true, true, "https://www.google.com/url?sa=i&url=https%3A%2F%2Ftx.audubon.org%2Fgreat-blue-heron-0&psig=AOvVaw3Sh2WAZ_x0oyqMH8-ZkHnU&ust=1747158690149000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCIjm68e_no0DFQAAAAAdAAAAABAM"));
        animal.add(new Bird ("Northern Cardinal", false, false, true, true, true, false, true, "https://www.scenichudson.org/wp-content/uploads/2022/11/scenichudson_20220138.jpg"));
        animal.add(new Bird ("Snowy Owl", false, false, true, true, true, true, false, "https://storage.googleapis.com/oceanwide_web/media-dynamic/cache/widen_1600/media/default/0001/27/2f13a82c7a97db96091530353598e744af74f917.jpeg"));
        
        animal.add(new Fish ("AngelFish", true, false, false, false, true, false, true, "https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Group_of_Pterophyllum_Altum.jpg/800px-Group_of_Pterophyllum_Altum.jpg"));
        animal.add(new Fish ("Eel", true, false, false, false, true, true, true, "https://www.nhm.ac.uk/content/dam/nhm-www/discover/electric-eels/electric-eel-full-body-freshwater-aquarium-two-column.jpg"));
        animal.add(new Fish ("Shark", true, false, false, false, true, true, false, "https://www.pbs.org/wnet/nature/files/2024/03/gerald-schombs-GBDkr3k96DE-unsplash-scaled-e1709848745953.jpg"));
        
        animal.add(new Reptile ("Alligator", true, false, false, false, true, true, false, "https://t4.ftcdn.net/jpg/00/77/00/71/360_F_77007154_YsFV9v7C1DtY9Xn8k6qzJ8GtkkOb0X0P.jpg"));
        animal.add(new Reptile ("Chameleon", false, false, false, false, true, true, true, "https://upload.wikimedia.org/wikipedia/commons/3/3d/Indian_chameleon_From_Kanakpura%2C_Karnataka.jpg"));
        
        animal.add(new Amphibian ("Frog", true, false, false, false, true, true, true, "https://ej9px6kfdm3.exactdn.com/wp-content/uploads/2022/12/Cute-Australian-Green-Tree-Frog-1024x683.jpeg?strip=all&lossy=1&quality=75&ssl=1"));
        
        System.out.println("\n\t\t\t\t\t\t\t\t\t\t Animal Guessing Game");
        System.out.println("\n\t\t\t\t\t\t\t\t\t\t\t\t . . .");
        System.out.println("\n\t\t\t\t\t\t\t\t\t\t\t    Welcome");
        
        System.out.println();
        System.out.println();
        System.out.println("\t\t\t\t\t\t\tYou may choose ONE animal out of the twenty listed\n\t\t\t\t\t\t\t\tWhat type of animal would you like?");
        System.out.println("And please note: \nWhen writing your responses, pay attention to clear instructions about grammer and capitalization. ALL answers are CAPS sensitive");
        System.out.println("\n\t\t\t\t\t\t\t\t\t\t\t    - Mammal \n\t\t\t\t\t\t\t\t\t\t\t    - Fish \n\t\t\t\t\t\t\t\t\t\t\t    - Bird \n\t\t\t\t\t\t\t\t\t\t\t    - Amphibian \n\t\t\t\t\t\t\t\t\t\t\t    - Reptile");
        
        System.out.println();
        System.out.println("Type your chosen animal type as it is written above^^");
        System.out.println();
        String n = scan.nextLine();
 
        
        System.out.println("Based on this list of your chosen animal type, what animal would you like to pick?");
        System.out.println();
        ArrayList<String> selectedList = new ArrayList<String>();
        for (int i = 0; i < animal.size(); i++){
            if (animal.get(i).getType().equals(n)){
                selectedList.add(animal.get(i).getAnimalName());
            }
        }
        System.out.println(selectedList);
        System.out.println();
        String pick = scan.nextLine();
        
        System.out.println();
        System.out.println("Great! Now here are some facts about the " + pick);
        System.out.println();
        
        for (int i = 0; i < animal.size(); i++){
            if (animal.get(i).getAnimalName().equals(pick)){
                System.out.println(animal.get(i).toString());
                System.out.println(animal.get(i).getImageLink());
            }
        }
        
        System.out.println("\n\n\nWhen you are ready to move on to the next step, type 'READY' in all caps to continue.\n");
        String ready = scan.nextLine();
        
        System.out.println("\nFor the following questions, please enter ONLY true or false in LOWERCASE.");
        
        System.out.println("\nNow that you have your animal picked along with some basic information . . .");
        System.out.println("\nLET THE GAME BEGIN!!");
        
        ArrayList<Animal> animalSort = animal;
        
        System.out.println("\n\nQuestion 1:");
        System.out.println("True or false: your animal likes the water");
        
        boolean answer1 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getIsWet() != answer1){
                animalSort.remove(i);
            }
        }
        
        System.out.println("\n\nQuestion 2:");
        System.out.println("True or false: your animal has fur");
        
        boolean answer2 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getIsFurry() != answer2){
                animalSort.remove(i);
            }
        }
        
        System.out.println("\n\nQuestion 3:");
        System.out.println("True or false: your animal has wings");
        
        boolean answer3 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getHasWings() != answer3){
                animalSort.remove(i);
            }
        }
        
        System.out.println("\n\nQuestion 4:");
        System.out.println("True or false: your animal is warm blooded");
        
        boolean answer4 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getIsWarmBlooded() != answer4){
                animalSort.remove(i);
            }
        }
        
        System.out.println("\n\nQuestion 5:");
        System.out.println("True or false: your animal lay eggs");
        
        boolean answer5 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getLaysEggs() != answer5){
                animalSort.remove(i);
            }
        }
        
        System.out.println("\n\nQuestion 6:");
        System.out.println("True or false: your animal is carnivorous(does your animal eat meat)?");
        
        boolean answer6 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getIsCarnivorous() != answer6){
                animalSort.remove(i);
            }
        }
        
        System.out.println("\n\nAnd finally, ");
        System.out.println("Question 7:");
        System.out.println("True or false: your animal has at least one color of the rainbow on its body");
        
        boolean answer7 = scan.nextBoolean();
        
        for (int i = animalSort.size() - 1; i >= 0; i--){
            if (animalSort.get(i).getIsColorful() != answer7){
                animalSort.remove(i);
            }
        }
        
        if (animalSort.size() > 1){
            System.out.println("Was your animal one of these options: " + animalSort);
        }
        else {
            System.out.println("Was your animal the: " + animalSort + "?");
        }
        
        String finalAnswer = scan.nextLine();
        
        System.out.println("\n\nThank you for playing this animal guessing game!!");
        System.out.println("\nIf you enjoyed this game, please give us a 5 star review on yelp!");
        System.out.println("\nAnd if you want to play again, just click the refresh button to start all over!!");
        System.out.println("\nGoodbye!");
    }
}
