# docker
### ✨ Simple example code (you can copy inside files)

**index.html**

```html
<!DOCTYPE html>
<html>
<head>
<title>Travel Agency</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Welcome to Dream Travel</h1>
<a href="about.html">About Us</a>
</body>
</html>
```

**about.html**

```html
<!DOCTYPE html>
<html>
<head>
<title>About Us</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<h1>About Our Travel Agency</h1>
<a href="index.html">Home</a>
</body>
</html>
```

**style.css**

```css
h1 { color: blue; }
body { font-family: Arial; }
```

---

# ✅ **STEP-2: Push Project Repository to GitHub**

### Initialize git

```
git init
git add .
git commit -m "First commit"
```

### Add GitHub repo

(Replace your link)

```
git remote add origin https://github.com/YOUR_USERNAME/travel-agency.git
```

### Push code

```
git branch -M main
git push -u origin main
```

---

# ✅ **STEP-3: Create Dockerfile**

Inside the project folder:

```
notepad Dockerfile
```

Paste this:

```dockerfile
FROM nginx:latest
COPY . /usr/share/nginx/html
```

Save and close.

---

# ✅ **STEP-4: Build Docker Image from GitHub Source**

### Clone your project from GitHub (optional)

```
git clone https://github.com/YOUR_USERNAME/travel-agency.git
cd travel-agency
```

### Build Docker image

```
docker build -t travel-agency:1.0 .
```

---

# ✅ **STEP-5: Run Docker Container**

```
docker run -d -p 8080:80 travel-agency:1.0
```

---

# ✅ **STEP-6: Verify Website**

Open browser and visit:

```
http://localhost:8080
```

