<!DOCTYPE html>
<html>
<head>
  <title>get_next_line 42 Project</title>
</head>
<body>
  <h1>get_next_line 42 Project</h1>
  
  <img src="https://images.velog.io/images/yamkim/post/635175a4-29ec-4a6c-bb0e-2feb21cbedf6/gnl_overview.png" alt="get_next_line 42 Project">
  
  <p>Welcome to the get_next_line 42 Project! This project is part of the 42 curriculum and focuses on creating a function that reads a line from a file descriptor.</p>

  <h2>About</h2>
  
  <p>The get_next_line 42 Project challenges you to create a function that reads a line from a file descriptor and stores it in a string. The function should handle different file descriptors, read buffer sizes, and multiple file reads. This project will enhance your understanding of file input/output operations and dynamic memory allocation.</p>

  <h2>Installation</h2>
  
  <ol>
    <li>Clone the repository:</li>
    <pre><code>git clone https://github.com/houssame-aithsain/get_next_line-42cursus.git</code></pre>
    <li>Change into the project directory:</li>
    <pre><code>cd get_next_line-42cursus</code></pre>
	  <pre><code>cd get_next_line</code></pre>
    <li>Compile the project:</li>
    <pre><code>gcc -Wall -Wextra -Werror -D BUFFER_SIZE=32 get_next_line.c get_next_line_utils.c</code></pre>
    <li>Once the compilation is complete, you can start using the get_next_line function in your projects.</li>
  </ol>

  <h2>Usage</h2>
  
  <p>To use the get_next_line function, include the appropriate header file in your code and call the function as needed:</p>
  
  <pre><code>#include "get_next_line.h"

int main(void) {
    int fd;
    char *line;

    fd = open("example.txt", O_RDONLY);
    if (fd == -1) {
        // handle file opening error
        return 1;
    }

    int ret = get_next_line(fd, &line);
    while (ret > 0) {
        printf("%s\n", line);
        free(line);
        ret = get_next_line(fd, &line);
    }

    if (ret == -1) {
        // handle reading error
        return 1;
    }

    close(fd);
    return 0;
}</code></pre>

  <h2>Documentation</h2>
  
  <p>The get_next_line function reads a line from the specified file descriptor and dynamically allocates memory to store the line. The function handles different file descriptors and buffer sizes defined by the BUFFER_SIZE macro. For detailed documentation and usage examples, refer to the project's documentation and the included <code>get_next_line.h</code> header file.</p>


  <h2>Contributing</h2>
  
  <p>Contributions to the get_next_line 42 Project are welcome! If you find any bugs, have suggestions for improvements, or want to add new features, please open an issue or submit a pull request. Make sure to follow the project's code style and guidelines.</p>
  
  <ol>
    <li>Fork the repository</li>
    <li>Create your feature branch (<code>git checkout -b feature/your-feature</code>)</li>
    <li>Commit your changes (<code>git commit -am 'Add some feature'</code>)</li>
    <li>Push to the branch (<code>git push origin feature/your-feature</code>)</li>
    <li>Open a pull request</li>
  </ol>

  <h2>License</h2>
  
  <p>The get_next_line 42 Project is open-source and is distributed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>. You can find the detailed license information in the <a href="https://github.com/your-username/get_next_line/blob/main/LICENSE">LICENSE</a> file.</p>
</body>
</html>
