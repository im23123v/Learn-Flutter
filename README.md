1. Hello World

// import 'package:flutter/material.dart';
// void main() {
//   runApp(MyApp());
// }
// class MyApp extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return MaterialApp(
//       home: Scaffold(
//         appBar: AppBar(title: Text("Hello World App")),
//         body: Center(
//           child: Text(
//             "Hello, Flutter!",
//             style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold),
//           ), ), ), );
//   }
// }


2. Plus++



// import 'package:flutter/material.dart';

// void main() => runApp(MaterialApp(home: CounterApp()));

// class CounterApp extends StatefulWidget {
//   @override
//   _CounterAppState createState() => _CounterAppState();
// }

// class _CounterAppState extends State<CounterApp> {
//   int count = 0;

//   @override
//   Widget build(BuildContext context) => Scaffold(
//         appBar: AppBar(title: const Text('Hello')),
//         body: Center(
//           child: Column(
//             mainAxisAlignment: MainAxisAlignment.center,
//             children: [
//               const Text('You have pushed the button this many times:'),
//               Text('$count', style: const TextStyle(fontSize: 30)),
//             ],
//           ),
//         ),
//         floatingActionButton: FloatingActionButton(
//           onPressed: () => setState(() => count++),
//           child: const Icon(Icons.add),
//         ),
//       );
// }



3. Login Form


//   import 'package:flutter/material.dart';
// void main() => runApp(LoginApp());
// class LoginApp extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return MaterialApp(
//       home: LoginPage(),
//     );
//   }
// }
// class LoginPage extends StatelessWidget {
//   final TextEditingController username = TextEditingController();
//   final TextEditingController password = TextEditingController();
//   @override
//   Widget build(BuildContext context) {
//     return Scaffold(
//       appBar: AppBar(title: Text("Login Form")),
//       body: Padding(
//         padding: const EdgeInsets.all(16),
//         child: Column(
//           children: [
//             TextField(controller: username, decoration: InputDecoration(labelText: "Username")),
//             TextField(controller: password, decoration: InputDecoration(labelText: "Password"), obscureText: true),
//             SizedBox(height: 20),
//             ElevatedButton(
//               onPressed: () {
//                 print("Username: ${username.text}, Password: ${password.text}");
//               },
//               child: Text("Login"),
//             ), ], ), ), );
//   }
// }



4. Two Screens



// import 'package:flutter/material.dart';
// void main() => runApp(NavigationApp());
// class NavigationApp extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return MaterialApp(home: FirstScreen());
//   }
// }
// class FirstScreen extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return Scaffold(
//       appBar: AppBar(title: Text("First Screen")),
//       body: Center(
//         child: ElevatedButton(
//           onPressed: () {
//             Navigator.push(
//                 context, MaterialPageRoute(builder: (context) => SecondScreen()));
//           },
//           child: Text("Go to Second Screen"),
//         ),  ),  );
//   }
// }
// class SecondScreen extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return Scaffold(
//       appBar: AppBar(title: Text("Second Screen")),
//       body: Center(
//         child: ElevatedButton(
//           onPressed: () => Navigator.pop(context),
//           child: Text("Back to First Screen"),
//         ), ), );
//   }
// }




5. Caliculator




// import 'package:flutter/material.dart';
// void main() => runApp(CalculatorApp());
// class CalculatorApp extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return MaterialApp(home: Calculator());
//   }
// }
// class Calculator extends StatefulWidget {
//   @override
//   _CalculatorState createState() => _CalculatorState();
// }
// class _CalculatorState extends State<Calculator> {
//   final num1 = TextEditingController();
//   final num2 = TextEditingController();
//   double result = 0;
//   void addNumbers() {
//     setState(() {
//       result = double.parse(num1.text) + double.parse(num2.text);
//     } );
//   }
//   @override
//   Widget build(BuildContext context) {
//     return Scaffold(
//       appBar: AppBar(title: Text("Simple Calculator")),
//       body: Padding(
//         padding: const EdgeInsets.all(16),
//         child: Column(
//           children: [
//             TextField(controller: num1, decoration: InputDecoration(labelText: "Enter first number"), keyboardType: TextInputType.number),
//             TextField(controller: num2, decoration: InputDecoration(labelText: "Enter second number"), keyboardType: TextInputType.number),
//             SizedBox(height: 20),
//             ElevatedButton(onPressed: addNumbers, child: Text("Add")),
//             Text("Result: $result", style: TextStyle(fontSize: 24)),
//           ], ), ), );
//   }
// }





6. Image + Emoji



// import 'package:flutter/material.dart';1. 
<!DOCTYPE html>
<html>
<body style="margin: 30%;">
<h2>Registration Form</h2>
<form>
  Name: <input type="text" name="name"><br>
  Email: <input type="email" name="email"><br>
  Password: <input type="password" name="password"><br>
  Gender: <input type="radio" name="gender">Male <input type="radio" name="gender">Female<br>
  <input type="submit" value="Register">
</form>
</body>
</html>


sudo apt install git -y
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bitwisebinary/devops.git
git push -u origin main


2.

# Setup
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Create or clone a repo
git init
git clone <repo_url>

# Check status and track files
git status
git add <filename>
git add .

# Commit changes
git commit -m "Your commit message"

# Branching
git branch
git branch <branch_name>
git checkout <branch_name>
git merge <branch_name>

# Connect to GitHub
git remote add origin <repo_url>
git push -u origin main
git pull origin main

# Logs and differences
git log
git diff

3.

git clone <URL>

4.  

# 1. Update packages
sudo apt update

# 2. Install Java (required for Jenkins)
sudo apt install openjdk-17-jdk -y

# 3. Add Jenkins repository key
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

# 4. Add Jenkins repo
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

# 5. Install Jenkins
sudo apt update
sudo apt install jenkins -y

# 6. Start and enable Jenkins
sudo systemctl enable jenkins
sudo systemctl start jenkins

# 7. Access Jenkins
sudo cat /var/lib/jenkins/secrets/initialAdminPassword




5)--- not yet confirmed

| Step | Command | Explanation |
|------|----------|-------------|
| *2. Initialize Git repository* | git init | Initializes a new local Git repository. |
| *3. Add files to staging* | git add . | Adds all files for commit. |
| *4. Commit changes* | git commit -m "Initial commit - Hello Jenkins" | Saves the staged files with a commit message. |

---

## ✅ FULL CLEANED + CORRECT COMMAND SEQUENCE

```bash
# --- Setup Java Project ---
mkdir jenkins-demo
cd jenkins-demo

# Create Hello.java
nano Hello.java
# Add this inside:
 public class Hello {
    public static void main(String[] args) {
         System.out.println("Hello Jenkins");
    }
 }

# --- Initialize Git ---
git init
git add .
git commit -m "Initial commit - Hello Jenkins"

# --- Connect to GitHub ---
git remote add origin <repository_URL>
git branch -M main
git push -u origin main

# --- Configure Jenkins ---
# 1. Open Jenkins Dashboard
# 2. Click "New Item" → Choose "Freestyle project"
# 3. Under "Source Code Management", select Git
# 4. Add repository URL and credentials

# --- Define Build Steps ---
echo "Building Java Project..."
javac Hello.java
echo "Running Project..."
java Hello

# --- Run Jenkins Job ---
# Click "Build Now"
# Jenkins console output:
# Building Java Project...
# Running Project...
# Hello Jenkins
# Finished: SUCCESS


6. # --- Install and setup Docker ---
sudo apt install docker.io -y
docker --version

sudo systemctl start docker
sudo systemctl enable docker
sudo systemctl status docker

sudo docker run hello-world

# --- Manage images ---
docker pull nginx
docker images


# --- Build custom image ---
nano Dockerfile
sudo docker build -t myapp .

# --- Run containers ---
docker run -d -p 8080:80 myapp
docker ps
docker ps -a

# --- Manage containers ---
docker stop <container_id>
docker start <container_id>
docker restart <container_id>
docker rm <container_id>
docker logs <container_id>

sudo docker run hello-world
sudo docker ps -a
sudo docker info
sudo docker start <id>
sudo docker run -d <image name>


7.


# 1. Create project folder
mkdir registration-form
cd registration-form

# 2. Start Docker service
sudo systemctl start docker
sudo systemctl enable docker
sudo systemctl status docker

# 3. Pull NGINX image
sudo docker pull nginx
sudo docker images

# 4. Create HTML file
nano register.html
# (Add your HTML form and save)

# 5. Create Dockerfile
nano Dockerfile
# Add:
FROM nginx:latest
COPY register.html /usr/share/nginx/html/index.html

# 6. Build Docker image
sudo docker build -t registrationform .

# 7. Run container
sudo docker run -d -p 8080:80 registrationform

# 8. Check running container
sudo docker ps

# 9. Open in browser
# Visit http://localhost:8080



7. (alternative)
Install Docker:

1. sudo apt update


2. sudo apt install docker.io -y



Start Docker:
3. sudo systemctl start docker
4. sudo systemctl enable docker
5. docker --version

Test Docker is working:
sudo docker run hello-world

★ Create a Simple Docker App

Create folder:
mkdir mydockerapp
cd mydockerapp

Create a Python file:
nano app.py
print("Hello from Docker!")
(Ctrl + S, Ctrl + X to save and exit)

Create Dockerfile:
nano Dockerfile
FROM python
COPY app.py .
CMD ["python", "app.py"]
(Ctrl + S, Ctrl + X to save and exit)

Build the Docker image:
sudo docker build -t myapp .

Run the container:
sudo docker run myapp

Output:
Hello from Docker!
// void main() => runApp(ImageApp());
// class ImageApp extends StatelessWidget {
//   @override
//   Widget build(BuildContext context) {
//     return MaterialApp(
//       home: Scaffold(
//         appBar: AppBar(title: Text("Image Example")),
//         body: Center(
//           child: Column(
//             mainAxisAlignment: MainAxisAlignment.center,
//             children: [
//               Icon(Icons.favorite, color: Colors.red, size: 60),
//               SizedBox(height: 20),
//               Image.network('https://flutter.dev/images/flutter-logo-sharing.png', width: 100),
//             ],   ),  ),  ),  );
//   }
// }
