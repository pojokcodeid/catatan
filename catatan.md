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
lalu jalankan ini
```
mvn exec:java -Dexec.mainClass=com.pojokcode.App
```

## linux spring boot run 
```
chmod +x mvnw
./mvnw spring-boot:run
```

## cara mengaktivekan snap install di WSL 2
- pastikan gunakan WSL terupdate
```
wsl --update
```
- masuk ke dir
```
sudo nvim /etc/wsl.conf
```
- isikan ini
```
[boot]
systemd=true
```
lalu jalankan ini
```
wsl.exe --terminate ubuntu / Ubuntu-22.04 (sesuaikan dengan nama distronya)
wsl --shutdown (dari wndows + r)
```

buka kembali ubuntu dari start menu
coba install sudo snap install htop

## uninstall distro dari WSL
1. Uninstall dari aplikasi (control panel)
2. wsl --list
3. wsl --unregister (nama distro dari list diatas)

## referensi
https://github.com/AdiCahyaSaputra/my-neovim-setup  <br>
https://github.com/Zeddnyx/Znvim  <br>
https://github.com/ChristianChiarulli/nvim  <br>
https://github.com/LunarVim/starter.lvim <br>
https://github.com/DaikyXendo/nvim-material-icon


Extension Wajib VS Code
```
1. One dark Pro
2. CFML
3. Auto Close Tag
4. Java Pack
5. Docker 
6. Fluent Icon
7. auto rename tag
8. Error Lens
9. Indent Rainbow
10 Live Server
11 Material Icon theme
12 PHP
13 Path Intelisense
14 Prettier
15 Rainbow bracket
16 Project manager For Java FX
17 WSL
18 Draw.io
19 MongoDB
20 eva theme
21 codeSnap
22 Errorlens
23 Code Runner
24 Quokka.js
25 Rest Client
26 Todo Hilight
27 Marquee
28 Import Cost
29 Code Time
30 ES7 React Snipets
```
## ini untuk membuat giagram gratis
```
https://app.diagrams.net/
```
## INstall google java format 
```
https://github.com/jose-elias-alvarez/null-ls.nvim/blob/main/doc/BUILTINS.md#formatting
https://www.npmjs.com/package/google-java-format
npm i -g google-java-format
```

# Install & Config Neovim Kali Linux
```
sudo dpkg -i ./nvim-linux64.deb
sudo apt install -f

sudo apt-get install git 

sudo apt install build-essential libssl-dev
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
source ~/.bashrc
nvm install 18.12.0

sudo apt-get install unzip
sudo apt-get install ripgrep
https://github.com/jesseduffield/lazygit#ubuntu

-- selanjutnya install config
```
