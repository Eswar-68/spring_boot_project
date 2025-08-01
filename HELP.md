# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/3.5.4/maven-plugin)
* [Create an OCI image](https://docs.spring.io/spring-boot/3.5.4/maven-plugin/build-image.html)

### Maven Parent overrides

Due to Maven's design, elements are inherited from the parent POM to the project POM.
While most of the inheritance is fine, it also inherits unwanted elements like `<license>` and `<developers>` from the parent.
To prevent this, the project POM contains empty overrides for these elements.
If you manually switch to a different parent and actually want the inheritance, you need to remove those overrides.

---

# 📘 Project Help Guide

## 📂 Project Structure
```text
src/
├── main/
│   ├── java/
│   └── resources/
├── test/
.idea/
pom.xml
````

## 🛠️ Setup Instructions

1. **Install Java 17+**

2. **Install Maven**

3. **Clone the project:**

   ```bash
   git clone https://github.com/Eswar-68/spring_boot_project.git
   cd spring_boot_project
   ```

4. **Build the project:**

   ```bash
   mvn clean install
   ```

5. **Run the project:**

   ```bash
   mvn spring-boot:run
   ```

## 🚀 Common Commands

| Task                | Command                  |
| ------------------- | ------------------------ |
| Build               | `mvn clean install`      |
| Run                 | `mvn spring-boot:run`    |
| Run Tests           | `mvn test`               |
| Update Dependencies | `mvn dependency:resolve` |

## ⚠️ Common Issues

| Error Message                  | Solution                                                     |
| ------------------------------ | ------------------------------------------------------------ |
| `java: package does not exist` | Check your `pom.xml` and reimport Maven.                     |
| Port already in use            | Change `server.port` in `application.properties`             |
| Git push error                 | Check if remote repo is added correctly with `git remote -v` |

## 🔗 Git Branch Notes

* **`main`**: Your primary branch now.

## 🧪 Testing

To run all tests:

```bash
  mvn test
  ```

## 🧠 Notes to Self

* IntelliJ config files are in `.idea/` (can be Git-ignored).
* `target/` is build output, should not be committed.
* Don’t forget to update `.gitignore` as needed.



## Stage, commit, and push the file

```bash
  git add help.md
  git commit -m "Add project help guide"
  git push origin main
````

---