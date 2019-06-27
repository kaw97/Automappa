## Autometa App
___

### Navigation and displaying some functionality:

![dashboard](images/autometaDashboard.gif "Autometa Dashboard")

___

### Autometa APP utilized as interactive interface for exploration and summaries of binning highly complex metagenomes.

___

## Usage:

Right now the autometa-app requires specific python libraries with specific versions of these libraries. There is a `requirements.txt` file within the repo that should be used to make sure the appropriate dependencies are satisfied. (In the future this will be all be contained in a docker image).

You can install all of these requirements with `pip`:

- `pip3 install -r requirements.txt`

Now that all of the dependencies are installed, you may run the app on your local machine or on the server.

#### Local:

```bash
python index.py </path/to/autometa_output.tsv>
```

#### Remote:

If you'd like to run the app on the server but view the output on your local machine, you first need to login to the server with a tunnel.

```bash
#ssh -L localport:127.0.0.1:serverport user@kwan-bioinformatics.pharmacy.wisc.edu
#example
ssh -L 6920:127.0.0.1:8050 jkwan@kwan-bioinformatics.pharmacy.wisc.edu
```

Now once you're on the server, navigate to your autometa-app repository and start the autometa-app server.

```bash
cd </path/to/autometa-app> && python index.py </path/to/autometa_output.tsv>
```

Navigate to the app view in your browser. This will correspond to the localport that was passed in upon login to the remote server. In the previous example above we would navigate to `127.0.0.1:6920`.

### Feature Requests, Issues, Bugs

I've integrated [Trello boards](https://trello.com/b/8LClJVKA "Link to Autometa-App Trello Board") into the bitbucket repository for noting any feature requests or bugs.
