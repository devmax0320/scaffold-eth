# 🏄‍♂️ Using Docker

Prerequisite: [Docker](https://docs.docker.com/engine/install/)/)

> clone/fork 🏗 scaffold-eth:

```bash
git clone https://github.com/austintgriffith/scaffold-eth.git
```

> run the script that builds the Docker image (takes some minutes to finish):

```bash
cd scaffold-eth/docker
./docker_build.sh
```

> [basic] run the script that spins the stack up and that's it (can take few seconds to set up):

```bash
./docker_run.sh
```

> [advanced] running front-end on a different port (eg. 8080):

```bash
docker run --name SCAFFOLD_ETH -e PORT=8080 -p 8080:8080 -p 8545:8545 -dt scaffold-eth
```

> [advanced] running the container in interactive mode (must run each tool manually):

```bash
docker run --name SCAFFOLD_ETH -p 3000:3000 -p 8545:8545 --entrypoint /bin/bash -ti scaffold-eth
```

🔏 Edit your smart contract `YourContract.sol` in `packages/hardhat/contracts`

📝 Edit your frontend `App.jsx` in `packages/react-app/src`

💼 Edit your deployment scripts in `packages/hardhat/deploy`

📱 Open http://localhost:3000 to see the app
