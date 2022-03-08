---
created: 2022-02-21T09:08:19.912Z
modified: 2022-02-21T11:13:29.331Z
---
Notes for David Smith:

front-end react (& redux) and argular.
back-end nodejs and python (django and flask).
worked with 3 evm networks, celo, reef, ewc.
either contractor or full-time is okay. workd part-time, want full time.
like talking to someone using his tool, and integrate feedbacks into the tool.

I like his resume :+1:

His portfolio:
Public repos:
* https://github.com/coolerwind/react-ecommerce
* https://github.com/coolerwind/fastfeet-mern

I looked at his portfolio.

It seems to me that his `ecommerce` project might be a fork of some other starter project https://github.com/reedbarger/ecommerce-react-graphql-stripe according to his [latest commit](https://github.com/coolerwind/react-ecommerce/commit/2565a75602f3dd98301b763fdb3a8d89d2f3b404), and the whole project was then modified and finished in 4 days. The front-end is written in React.js. I couldn't tell much, but I think he is okay with React.js.
Btw I am quite shocked that there are so many e-commerce projects :joy: . **David Carlisle** also had one. There are many similar e-commerce on GitHub as well.

As for his second project, `fastfeet-mern`, it seems to me there are many fastfeet projects [on GitHub](https://github.com/search?q=fastfeet) as well that have similar file structures. I didn't look in to the details. The project might be some sort of code challenges. So it's hard for me to judge much from this project.

I would suggest we ask the our candidates to do a simple code challenging project that will take around 1-2 days to finish, but I am not sure if they will be willing to do so or not :joy:

Below is my idea of the code challenging project:

---

Finish a Todo app that lives on blockchain:

You will store the user's Todo items on a Solidity smart contract deployed on any EVM compatible (testing) network, such as Ethereum Ropsten Testnet, Ethereum Rinkeby Testnet, Polygon Mumbai Testnet, etc.

Requirements:
1. The front-end needs to be written using React.js, preferrably using the functional components and hooks instead of the class components.
2. The front-end needs to be able to connect to the MetaMask wallet and display the address of the connected wallet.
3. The Todo app does the following jobs:
   1. Add a new Todo item. The Todo item is just a string, and initially "not completed".
   2. Toggle a Todo item as "completed" or "not completed". Only the owner of the Todo item can do that.
   3. List all Todo items by time created desc, both "completed" and "not completed".  Everyone should be able to view, not only the owner.
       You should have a URL like `/todo/:wallet-address` that allows people to view the Todo items of the given wallet address.

Bonus point:
  * Allow the user to view separately the "completed" Todo items, "not completed" Todo items, and both.
  * Add pagination to view the Todo items. For example, each page will display 5 Todo items, and user could choose to view the first, the second, ... page
  * Display the total number of users (wallet addresses) that ever created Todo items.
  * Delete an existing Todo item. Only the owner of the Todo item can do that.

Please host your front-end work on GitHub Pages preferably or anywhere else such as Heroku, Firebase and send us the link.
Please also send us the address of your deployed Todo smart contract and the code.
Please also show us your front-end code.

---

What do you guys think? :joy: Would that be too much?