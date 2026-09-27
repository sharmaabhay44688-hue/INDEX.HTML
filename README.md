# INDEX.HTML<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Client-Server Architecture & DNS</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background: #f4f7fb;
            color: #06490a;
        }

        header {
            background: #d204d2;
            color: white;
            text-align: center;
            padding: 35px 20px;
        }

        header h1 {
            margin-bottom: 10px;
        }

        .container {
            width: 90%;
            max-width: 1000px;
            margin: 30px auto;
        }

        section {
            background: rgb(189, 184, 184);
            padding: 25px;
            margin-bottom: 25px;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
        }

        h2 {
            color: #47002b;
            margin-bottom: 15px;
        }

        h3 {
            margin-top: 20px;
            margin-bottom: 10px;
            color: #4e0544;
        }

        ul, ol {
            margin-left: 25px;
            margin-bottom: 15px;
        }

        .architecture {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin: 25px 0;
            flex-wrap: wrap;
        }

        .box {
            padding: 20px 30px;
            border-radius: 8px;
            text-align: center;
            font-weight: bold;
            border: 2px solid #e904d2;
        }

        .arrow {
            font-size: 30px;
            font-weight: bold;
        }

        .example {
            background: #eef2ff;
            padding: 15px;
            border-left: 5px solid #fc18f8;
            margin-top: 15px;
        }

        code {
            background: #eee;
            padding: 3px 6px;
            border-radius: 4px;
        }

        footer {
            text-align: center;
            background: #683654;
            color: rgba(78, 4, 252, 0.374);
            padding: 20px;
            margin-top: 30px;
        }

        @media (max-width: 600px) {
            .arrow {
                transform: rotate(90deg);
            }
        }
    </style>
</head>

<body>

<header>
    <h1>Client-Server Architecture & DNS</h1>
    <p>Basic of web Development Assignment</p>
</header>

<div class="container">

    <section>
        <h2>1. Client-Server Architecture</h2>

        <p>
            Client-Server Architecture is a network model in which a
            client requests services or resources from a server, and
            the server processes the request and sends a response back
            to the client.
        </p>

        <div class="architecture">
            <div class="box">Client<br><small>Browser / App</small></div>

            <div class="arrow">→</div>

            <div class="box">Server<br><small>Processes Request</small></div>

            <div class="arrow">→</div>

            <div class="box">Response</div>
        </div>

        <h3>What is a Client?</h3>
        <p>
            A client is a device or application that sends a request
            to a server to access a service or resource.
            Examples include web browsers, mobile applications,
            and desktop applications.
        </p>

        <h3>What is a Server?</h3>
        <p>
            A server is a computer or system that receives requests
            from clients, processes them, and provides the requested
            data or service.
        </p>

        <h3>How Does It Work?</h3>

        <ol>
            <li>The client sends a request to the server.</li>
            <li>The server receives the request.</li>
            <li>The server processes the request.</li>
            <li>The server sends a response.</li>
            <li>The client displays the result to the user.</li>
        </ol>

        <div class="example">
            <strong>Example:</strong>
            When you open a website in Chrome, Chrome acts as the
            client. It sends a request to the website's server.
            The server sends the webpage back to Chrome.
        </div>
    </section>

    <section>
        <h2>2. Advantages of Client-Server Architecture</h2>

        <ul>
            <li>Centralized data management</li>
            <li>Better security and access control</li>
            <li>Easy data backup and maintenance</li>
            <li>Multiple clients can access the same server</li>
            <li>Resources can be managed centrally</li>
        </ul>

        <h3>Disadvantages</h3>

        <ul>
            <li>Server failure can affect multiple clients.</li>
            <li>Server maintenance can be expensive.</li>
            <li>Heavy traffic can slow down the server.</li>
        </ul>
    </section>

    <section>
        <h2>3. DNS (Domain Name System)</h2>

        <p>
            DNS stands for <strong>Domain Name System</strong>.
            It is a system that converts human-readable domain names
            into IP addresses that computers can understand.
        </p>

        <div class="example">
            <strong>Example:</strong><br>
            Domain Name: <code>google.com</code><br>
            DNS finds the corresponding IP address of the server.
        </div>

        <h3>Why is DNS Needed?</h3>

        <p>
            Computers communicate using IP addresses, but remembering
            numerical IP addresses for every website would be difficult.
            DNS allows users to access websites using easy-to-remember
            domain names.
        </p>
    </section>

    <section>
        <h2>4. How DNS Works</h2>

        <div class="architecture">
            <div class="box">User</div>
            <div class="arrow">→</div>
            <div class="box">DNS Resolver</div>
            <div class="arrow">→</div>
            <div class="box">DNS Server</div>
            <div class="arrow">→</div>
            <div class="box">IP Address</div>
        </div>

        <ol>
            <li>User enters a domain name in the browser.</li>
            <li>The browser checks its DNS cache.</li>
            <li>A DNS resolver searches for the IP address.</li>
            <li>DNS servers help find the correct IP address.</li>
            <li>The IP address is returned to the client.</li>
            <li>The browser connects to the web server.</li>
            <li>The website is displayed to the user.</li>
        </ol>
    </section>

    <section>
        <h2>5. Main Components of DNS</h2>

        <h3>1. DNS Resolver</h3>
        <p>
            The resolver receives the DNS query from the client and
            searches for the required IP address.
        </p>

        <h3>2. Root DNS Server</h3>
        <p>
            Root servers provide information about the appropriate
            Top-Level Domain (TLD) servers.
        </p>

        <h3>3. TLD Server</h3>
        <p>
            TLD servers handle domains such as .com, .org, .net,
            .in, and others.
        </p>

        <h3>4. Authoritative DNS Server</h3>
        <p>
            The authoritative server contains the actual DNS records
            for a domain and provides the requested information.
        </p>
    </section>

    <section>
        <h2>6. Common DNS Records</h2>

        <ul>
            <li><strong>A Record:</strong> Maps a domain to an IPv4 address.</li>
            <li><strong>AAAA Record:</strong> Maps a domain to an IPv6 address.</li>
            <li><strong>CNAME:</strong> Creates an alias for another domain.</li>
            <li><strong>MX Record:</strong> Specifies mail servers for a domain.</li>
        </ul>
    </section>

    <section>
        <h2>7. Relationship Between Client-Server Architecture and DNS</h2>

        <p>
            DNS and Client-Server Architecture work together when
            accessing websites. DNS helps the client find the IP
            address of the server, and then the client communicates
            with that server to request and receive website data.
        </p>

        <div class="architecture">
            <div class="box">Browser<br>(Client)</div>
            <div class="arrow">→</div>
            <div class="box">DNS</div>
            <div class="arrow">→</div>
            <div class="box">IP Address</div>
            <div class="arrow">→</div>
            <div class="box">Web Server</div>
        </div>
    </section>


    <!-- Conclusion -->
    <section>
        <h2>8. Conclusion</h2>

        <p>
            Client-Server Architecture is an important model used
            for communication between clients and servers.
            DNS is an essential internet service that converts
            domain names into IP addresses. Together, they make
            accessing websites and online services easier and more
            efficient for users.
        </p>
    </section>

</div>

<footer>
    <p>Basic of Web Development Assignment | Client-Server Architecture & DNS</p>
</footer>

</body>
</html>
