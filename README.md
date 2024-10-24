# Praktikum 3
## Nama  : Yusdiansyah Andika Haryo Saputra
## NIM : 312310650
## Kelas : TI.23.A.6

# Inheritance

## Class Pegawai
```java

public class pegawai{
    private String nama;
    private double gajipokok;

    public void setNama(String nama){
        this.nama = nama;
    }

    public String getNama(){
        return this.nama;
    }

    public void setGajipokok(double gajipokok){
        this.gajipokok = gajipokok;
    }
    public double getGajipokok(){
        return this.gajipokok;
    }

    public void Cetakinfo(){
        System.out.println("Nama: "+ nama);
        System.out.println("Gaji Pokok: "+ gajipokok);
    }
}
```

## Class Manager
```java

public class Manager extends pegawai {
    private double tunjangan;
    
    public void setTunjangan(double tunjangan){
        this.tunjangan = tunjangan;
    }

    public double getTunjangan(){
        return this.tunjangan;
    }

    @Override
    public void Cetakinfo(){
        super.Cetakinfo();

        System.out.println("Tunjangan: " + tunjangan);
    } 

    public void cetakTunjangan(){
        System.out.println("Tunjangan: "+ tunjangan);
    }
}
```

## Class Programmer
```java

public class Programmer extends pegawai {
    private double bonus;

    public void setBonus(double bonus){
        this.bonus = bonus;
    }

    public double getBonus(){
        return this.bonus;
    }

    @Override
    public void Cetakinfo(){
        super.Cetakinfo();

        System.out.println("Bonus: " + bonus);
    }

    public void CetakBonus(){
        System.out.println("Bonus: " + bonus);
    }
}
```

## Main Class
```java

public class main {
    public static void main(String[] args) {
        Manager manager = new Manager();

        manager.setNama("menej");
        manager.setGajipokok(8000000);
        manager.setTunjangan(2000000);
        manager.Cetakinfo();

        Programmer programmer = new Programmer();

        programmer.setNama("Geymer");
        programmer.setGajipokok(7000000);
        programmer.setBonus(2000000);
        programmer.Cetakinfo();
    }
}
```
