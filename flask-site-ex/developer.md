We begin with this file structure:
$> tree -L 2
    .
    ├── Dockerfile
    ├── app.py
    ├── developer.md
    ├── requirements.txt
    └── templates
        └── index.html

    1 directory, 5 files

Then we run the following, note the ".":
$> docker build -t your-docker-username-goes-here/catnip .

If you don't already have certain images downloaded it will grab them automatically.

Make sure your image appears  under the name "your-docker-username-goes-here/catnip" 
$> docker images

Check to see it actually works:
docker run -p 8888:5000 yourusername/catnip


