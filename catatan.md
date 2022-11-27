## Install Eclipse Di Ubunut WSL 2
```
sudo apt install libswt-gtk-4-jni
sudo apt update
sudo apt install default-jre
sudo apt install openJdk18
sudo snap install --classic eclipse
eclipse
```

## Cara Jalankan Springboot dari Maven
```
mvn spring-boot:run
```
## Cara Membuat Projek Maven
```
mvn archetype:generate -DgroupId=latihan1 -DartifactId=DemoMavenProject -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```
atau 
```
mvn -B archetype:generate -DgroupId='com.pojokcode' -DartifactId=mvn-example -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion='1.4'
```

## menalankan maven projeck
-- tambahkan dulu code berikut pada pom.xml
```
 <plugin>
    <!-- Build an executable JAR -->
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-jar-plugin</artifactId>
    <version>3.1.0</version>
    <configuration>
      <archive>
        <manifest>
          <addClasspath>true</addClasspath>
          <!-- here we specify that we want to use the main method within the App class -->
          <mainClass>com.pojokcode.App</mainClass>
        </manifest>
      </archive>
    </configuration>
  </plugin>
```
```
mvn exec:java -Dexec.mainClass=com.pojokcode.App
```

## linux spring boot run 
```
chmod +x mvnw
./mvnw spring-boot:run
```

----cara mengaktivekan snap istall di WSL 2
-- pastikan gunakan WSL terupdate
wsl --update
--masuk ke dir
sudo nvim /etc/wsl.conf
--isikan ini
[boot]
systemd=true

wsl.exe --terminate ubuntu / Ubuntu-22.04 (sesuaikan dengan nama distronya)
wsl --shutdown (dari wndows + r)

buka kembali ubuntu dari start menu
coba install sudo snap install htop

---- uninstall distro dari WSL
1. Uninstall dari aplikasi (control panel)
2. wsl --list
3. wsl --unregister (nama distro dari list diatas)