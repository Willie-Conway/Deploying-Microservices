# 🎶 Deploying Songs Microservices 🎵

Welcome to the **Songs Microservice**! This is a simple microservice that provides access to a collection of songs. It's built using **Flask** and connects to a **MongoDB** database to store song information. 🚀

 ![Deploying the Songs microservice on RedHat OpenShift](https://github.com/Willie-Conway/Deploying-Microservices/blob/7e4823a837bebd85a39ae6fbdf5e5747d837de9e/Screenshots/Deploying%20the%20Songs%20microservice%20on%20RedHat%20OpenShift.gif)

## 💡 Features
- 🎤 **Add songs** to the database.
- 🎧 **Retrieve all songs** from the database.
- 🎶 **Health Check** endpoint to verify the service is up and running.

## 🛠️ Technologies Used
- **Python** 🐍
- **Flask** 🐚
- **MongoDB** 🗃️
- **OpenShift** ☁️
- **GitHub** 💻

## 📦 Setup Instructions

### 1️⃣ Clone the Repository
Clone the repository to your local machine:

```bash
git clone https://github.com/Willie-Conway/Deploying-Microservices.git
```

### 2️⃣ Install Dependencies
Navigate to the project directory and set up a virtual environment:

```bash
cd Back-End-Development-Songs
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```

### 3️⃣ Configure MongoDB
Ensure that the MongoDB service is up and running. Use the internal MongoDB URL for OpenShift or any other connection string.

Example MongoDB URL:
```
mongo.sn-labs-captainfedo1.svc.cluster.local
```

### 4️⃣ Running the Service Locally
To run the microservice locally:

```bash
python app.py
```

Visit `http://localhost:5000` to see the service in action! 🎉

### 5️⃣ Deploy to OpenShift
To deploy the microservice to OpenShift, use the following command:

```bash
oc new-app https://github.com/${GITHUB_ACCOUNT}/Back-End-Development-Songs --strategy=source --name=songs --env MONGODB_SERVICE=mongo.${OPENSHIFT_PROJECT}.svc.cluster.local --name songs
```

## 🌐 Accessing the Service

Once deployed, you can access the Songs microservice via the following URL:

```text
http://songs-sn-labs-captainfedo1.labs-prod-openshift-san-a45631dc5778dc6371c67d206ba9ae5c-0000.us-east.containers.appdomain.cloud
```

Use the `/health` endpoint to check if the service is running smoothly:

```text
http://songs-sn-labs-captainfedo1.labs-prod-openshift-san-a45631dc5778dc6371c67d206ba9ae5c-0000.us-east.containers.appdomain.cloud/health
```

It will return a response like:
```json
{
  "status": "OK"
}
```

## 🚧 Contributing

If you'd like to contribute, feel free to open an issue or pull request. 😊

1. Fork the repo 🍴
2. Create your feature branch 🧑‍💻
3. Commit your changes ✍️
4. Push to the branch 🚀
5. Open a pull request 👥

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 📝

## 💬 Contact

For any questions or suggestions, feel free to reach out to me via:

- Email: hire.willie.conway@gmail.com 📧
- GitHub: [Willie-Conway](https://github.com/Willie-Conway) 👨‍💻

Happy coding! 🎉

### Key Sections:

1. **Project Title**: Includes a title with relevant emojis.
2. **Features**: Highlights features of the project using emojis.
3. **Technologies Used**: Mentions technologies with related emojis.
4. **Setup Instructions**: Describes how to clone, install, and run the project.
5. **Deployment**: Explains how to deploy the microservice to OpenShift.
6. **Accessing the Service**: Includes details on how to access the health endpoint.
7. **Contributing**: A friendly guide for contributing.
8. **License**: States the project license.
9. **Contact**: Information on how to contact the developer.
