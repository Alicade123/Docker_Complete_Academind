### First nodejs docker app setup

##Set up

```bash
npm init -y
npm install express
```

### run
```bash
docker build .
docker run -p 3000:3000 my-express-app
```

## Alternatives

#### Clean Rebuild and LaunchBecause you altered both the package.json and the Dockerfile, force a completely fresh image build:

```bash
docker build --no-cache -t my-express-app .
```

#### Rebuild your Docker ImageSince you modified any file in app, rebuild your container so Docker pulls in the fixed script:

```bash
docker build -t my-express-app .
```
