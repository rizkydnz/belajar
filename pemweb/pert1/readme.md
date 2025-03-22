<table>
            <tr>
                <th>Company</th>
                <th>Contacts</th>
                <th>Country</th>
            </tr>
            <tr>
                <td>Alfreds Futterkiste</td>
                <td>Maria Anders</td>
                <td>Germany</td>
            </tr>
            <tr>
                <td>Centro Comercial Mocteruma</td>
                <td>Francisco Chang</td>
                <td>Mexico</td>
            </tr>
        </table>




/* Reset default padding dan margin */
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #d0d0d0;
    color: #333;
    text-align: center;
}

/* Styling untuk content utama */
.content_1 {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    margin: 10% auto;
    padding: 20px;
    background-color: aquamarine;
    width: 80%;
    border-radius: 10px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
}

.content_1 .content_2 {
    padding: 20px;
}

h1 {
    font-size: 24px;
    margin-bottom: 10px;
}

h2 {
    font-size: 18px;
    font-weight: normal;
    margin-bottom: 5px;
}

h3 {
    font-size: 14px;
    font-weight: bold;
    margin-top: 10px;
}

/* Styling tabel dengan solid border */
.table-container {
    margin: 30px auto;
    width: 80%;
    overflow-x: auto;
}

.table-style {
    width: 100%;
    border-collapse: collapse;
    background: white;
    border-radius: 10px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
}

.table-style th,
.table-style td {
    padding: 12px;
    border: 2px solid #333; /* Solid border seperti Tailwind */
    text-align: center;
}

.table-style th {
    background-color: #3882f6;
    color: white;
    font-weight: bold;
}

.table-style tr:nth-child(even) {
    background-color: #f8f9fa;
}

.table-style tr:hover {
    background-color: #e2e8f0;
    cursor: pointer;
}

/* Styling form container */
.form-container {
    margin: 30px auto;
    width: 80%;
    max-width: 400px;
    padding: 20px;
    background: white;
    border-radius: 10px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
}

/* Styling form input */
.form-container form {
    display: flex;
    flex-direction: column;
}

.form-container label {
    font-size: 14px;
    font-weight: bold;
    margin: 10px 0 5px;
    color: #333;
}

.form-container input {
    padding: 10px;
    font-size: 14px;
    border: 2px solid #ccc; /* Solid border seperti Tailwind */
    border-radius: 5px;
    outline: none;
    transition: border 0.3s ease;
}

.form-container input:focus {
    border-color: #4CAF50;
    box-shadow: 0 0 5px rgba(76, 175, 80, 0.5);
}

/* Styling tombol submit */
.form-container button {
    margin-top: 15px;
    padding: 10px;
    font-size: 16px;
    font-weight: bold;
    color: white;
    background-color: #4CAF50;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s ease;
}

.form-container button:hover {
    background-color: #388E3C;
}






version: '3'

services:
  webserver:
    container_name: webserver
    image: nginx
    ports:
      - 80:80
    volumes:
      - ./src:/usr/share/nginx/html



COMPOSE_PROJECT_NAME=belajar
IMAGE_TAG=latest