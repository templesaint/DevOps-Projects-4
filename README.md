# DevOps-Projects-4



# Project 4: MEAN Stack Deployment on AWS EC2

This repository documents the end-to-end deployment of a Book Management application using the **MEAN stack** (MongoDB, Express.js, Angular, and Node.js) on an Ubuntu-based AWS EC2 virtual environment. 

---

## Architecture Overview

The application utilizes a classic 3-tier architecture:
*   **Presentation Layer:** Built with Angular to provide a responsive user interface.
*   **Application Layer:** Powered by Node.js and Express.js to handle business logic and API routing.
*   **Data Layer:** Supported by MongoDB for flexible, document-based data storage.



---



## Deployment Steps & Visual Documentation



### Step 1: Provisioning the Infrastructure
First, an Ubuntu Server instance was launched on AWS EC2 to host the entire stack.

*   **Instance Lifecycle:** Verifying that the virtual machine is successfully running and active.
    ![AWS EC2 Instance Running](<../Desktop/IMAGES-P4/1. AWS EC2 INSTANCE Running.png>)

*   **Network Configuration:** Locating the public IP address assignment for remote communication.
    ![AWS EC2 Instance IP Address](<../Desktop/IMAGES-P4/2. AWS EC2 Instance showing IP address.png>)


---

### Step 2: Server Access and Environment Provisioning
Secure Shell (SSH) was used to access the remote terminal, followed by setting up the core application runtimes.

*   **Remote Connection:** Accessing the Ubuntu instance via a local terminal environment.
    ![SSH Ubuntu Terminal Login](<../Desktop/IMAGES-P4/3. SSH Ubuntu terminal login.png>)


*   **Node.js Installation:** Deploying the Node.js JavaScript runtime environment.
    ![Node.js Installed](<../Desktop/IMAGES-P4/4. Node js installed .png>)


*   **Package Management:** Verification of the Node Package Manager (NPM) setup.
    ![NPM Installed](<../Desktop/IMAGES-P4/6. npm installed .png>)


---

### Step 3: Database Installation and Configuration
MongoDB was installed and configured locally on the server to serve as our backend database management system.

*   **Database Status:** Ensuring the MongoDB daemon engine is active, running, and listening for local network connections.
    ![MongoDB Server Up and Running](<../Desktop/IMAGES-P4/5. MogoDB Server up and Running.png>)



---

### Step 4: Backend Application and Router Implementation
The application files were created to initiate the server backend and map out the application's API endpoints.

*   **Server Entry Point:** Baseline setup of the primary `server.js` file.
    ![Server.js File Initial](<../Desktop/IMAGES-P4/7. server.js file.png>)


*   **Database & Server Refinement:** Enhancements applied to the backend `server.js` architecture for stable database initialization.
    ![Corrected Server.js File](<../Desktop/IMAGES-P4/8. corrected server.js file .png>)


*   **API Routing Matrix:** Establishing database schema mappings and route handlers inside the `routes.js` file.
    ![Routes.js File Initial](<../Desktop/IMAGES-P4/9. routes.js file .png>)


*   **Syntax Correction:** Debugging and resolving syntax issues inside `routes.js` to ensure proper execution.
    ![Corrected Routes.js Syntax](<../Desktop/IMAGES-P4/10. corrected routes.js  syntx to help node js run successfully.png>)



---

### Step 5: Application Execution & Port Binding
With the backend properly configured, the Node application was spun up to listen for requests.


*   **Local Service Runtime:** Running the Express server successfully on the designated internal application port (Port `3300`).
    ![Node Server Running at Port 3300](<../Desktop/IMAGES-P4/11. node server.js running at port 3300.png>)


---

### Step 6: Security and Firewall Configurations
By default, AWS blocks external HTTP access to non-standard ports. An explicit rule was required to allow public incoming traffic.

*   **Security Group Definition:** Creating an inbound network access rule within the AWS management console.
    ![Inbound Rule Definition](<../Desktop/IMAGES-P4/12. inbound rule.png>)


*   **Port 3300 Permission:** Finalized Security Group state opening traffic access for Port `3300`.
    ![AWS Security Group Rules](<../Desktop/IMAGES-P4/13. AWS EC2 Instance security rule permission port 3300.png>)



---

### Step 7: Production Verification
The application setup was verified by hitting the instance's public IP address via an external browser interface.

*   **End-to-End Delivery:** The Books Management site loading and rendering successfully via the public web on Port `3300`.
    ![Books Site Rendering](<../Desktop/IMAGES-P4/14. Books site showing on brower at port 3300.png>)


---

## Conclusion
The MEAN Stack application is fully functional, properly exposed through cloud network security protocols, and communicating with its dedicated MongoDB database tier successfully.
