# **Study-Buddy: AI-Powered Multi-Agent Learning System on GCP**



**Study-Buddy** is a cloud-native, AI-driven educational platform that leverages **multi-agent systems** to provide intelligent tutoring, curriculum planning, and automated assessment capabilities. Built on **Google Cloud Platform (GCP)**, it integrates AI-powered services with scalable cloud infrastructure to create seamless and intelligent learning experiences.

---

## Video Demo
[![image](https://github.com/user-attachments/assets/6c4d6dca-4750-4758-8e46-b557fb9d6ec6)](https://youtu.be/N6aqf_-K5qI)


## **🚀 Key Features**

✅ **AI-Powered Learning Portal** – Interactive quizzes, auto-graded assignments, and AI-assisted tutoring with Gemini models.  
✅ **Intelligent Curriculum Planning** – AI-driven course generation, book recommendations, and structured learning paths.  
✅ **Automated Grading & Feedback** – Vertex AI-powered evaluation for assignments and student responses.  
✅ **Cloud-Native Microservices** – Containerized architecture for independent and scalable components.  
✅ **Event-Driven Workflows** – Uses Pub/Sub and Cloud Functions for seamless system integration.  
✅ **Scalable Deployment on GCP** – Managed services with auto-scaling using Cloud Run, Compute Engine, and Kubernetes.

---

## **🛠 Cloud Architecture & Deployment on GCP**

The platform follows a **microservices and multi-agent** architecture, where each service is independently containerized, deployed, and managed via **Google Kubernetes Engine (GKE)** and **Cloud Run**.

### **🔹 Core GCP Services Used:**

- **Vertex AI** – Hosts Gemini models for AI-driven tutoring, automated grading, and curriculum recommendations.
- **Cloud Run** – Deploys lightweight microservices with auto-scaling.
- **Compute Engine** – Provides dedicated VMs for running intensive AI workloads.
- **Cloud Functions** – Event-driven processing for quizzes, assignments, and student tracking.
- **BigQuery** – Manages structured learning data and analytics.
- **Cloud Storage** – Secure storage for course materials and student records.
- **Pub/Sub** – Enables asynchronous communication between multi-agent components.
- **LangChain + LangGraph** – Orchestrates interactions between AI models and cloud services.

---

## **📌 Project Structure**

```
📦 study-buddy
├── portal/          # AI-powered learning interface (Flask, Vertex AI, Firebase)
├── planner/         # Intelligent curriculum planning (Compute Engine, Vertex AI, Firestore)
├── courses/         # Course management system (Cloud Storage, Firestore, AI metadata tagging)
├── assignment/      # AI-driven grading & feedback (Cloud Functions, BigQuery, Gemini AI)
├── bookprovider/    # AI-powered book recommendations (Cloud Run, Firestore, Vertex AI)
├── setup/           # Initialization and configuration scripts
├── README.md        # Project documentation
```

---

## **📌 Service Breakdown & Cloud Integration**

### **1️⃣ Portal (`/portal`) – AI-Powered Learning Interface**  
📍 **Hosted on:** Cloud Run  
📍 **AI Capabilities:** Gemini models for real-time Q&A and content recommendations  
📍 **Features:**
- Dynamic course delivery & interactive quizzes  
- AI-assisted answer evaluation  
- Auto-generated teaching plans  
- Secure authentication via Firebase  

### **2️⃣ Planner (`/planner`) – Intelligent Curriculum AI**  
📍 **Hosted on:** Compute Engine + Vertex AI  
📍 **Features:**
- AI-powered curriculum generation & personalization  
- Book and resource recommendations via AI search models  
- Automated course structuring using Google Cloud SQL  

### **3️⃣ Courses (`/courses`) – Cloud-Native Course Management**  
📍 **Hosted on:** Cloud Run + Cloud Storage  
📍 **Features:**
- Stores course materials in Cloud Storage  
- Organizes and retrieves resources using Firestore DB  
- Uses AI for metadata tagging and smart search  

### **4️⃣ Assignment (`/assignment`) – AI-Driven Grading & Feedback**  
📍 **Hosted on:** Cloud Functions + Vertex AI  
📍 **Features:**
- AI-based grading via Gemini & DeepSeek  
- Student submission tracking with BigQuery  
- Real-time feedback generation  

### **5️⃣ Book Provider (`/bookprovider`) – AI-Powered Reading Suggestions**  
📍 **Hosted on:** Cloud Run + AI Recommendations API  
📍 **Features:**
- AI-driven book recommendations  
- Catalog stored in Firestore  
- Personalized reading suggestions via Vertex AI  

---

## **🔧 Setup & Deployment**

### **1️⃣ Prerequisites**
- Google Cloud Platform (GCP) account
- Python 3.9+
- Docker & Cloud SDK installed

### **2️⃣ Clone the Repository**
```sh
 git clone https://github.com/yourusername/study-buddy.git
 cd study-buddy
```

### **3️⃣ Install Dependencies**
```sh
pip install -r requirements.txt
```

### **4️⃣ Deploy Services to Google Cloud**
```sh
# Deploy Portal
 gcloud run deploy study-buddy-portal --source=portal

# Deploy Planner
 gcloud compute instances create study-buddy-planner --source=planner

# Deploy Assignments
 gcloud functions deploy study-buddy-assignments --runtime python39 --trigger-http
```

### **5️⃣ Access the Platform**
After deployment, access the **Study-Buddy** UI via the Cloud Run service URL or set up a custom domain.

```sh
gcloud run services list  # Find the deployed service URL
```

---
