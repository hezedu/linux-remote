# linux-remote
Make you Linux sever GUI in on minite.
A Webside Remote Desktop of Linux.

## Requested
- Linux.
- [Node.js](https://nodejs.org) 8+. and ensure all users are available.

## Browsers Compatibility
Latest **Chrome** And Latest **Firefox** work fine. 

Not ___IE___.

**Edge** and **Safari** unknown(it should be OK).

## Online Demo
https://demo.linux-remote.org

<br>

## Install
**Step 1:**

`cd /opt/ && sudo git clone --depth 1 https://github.com/linux-remote/linux-remote.git && cd linux-remote`

or:<br>
`cd /opt/ && sudo wget https://github.com/linux-remote/linux-remote/archive/master.zip -O "linux-remote.zip" && sudo unzip -q linux-remote.zip && sudo mv linux-remote-master linux-remote && sudo rm linux-remote.zip  && cd linux-remote`

<i>/opt</i> dir only writable for root. so you should use: `sudo`
<br>

**Step 2:**  `sudo node init`

It will generate config.js, and set permission: Only `root` users can read it..

<br>

**Step 3:** `npm install`

<br>

## Setting

modify `./config.js`:
```js
module.exports = {
  port: 3001, // Website listen port. default: 3001

  sshPort: 22, // SSH server listen port, default: 22

  ssl : null, // http model, Unsafe,  default: null.
  /*
  ssl: {  // Or provide an Object {cert, key} to enter https model: 
    cert: '/somedir/cert.pem',
    key: '/somedir/privkey.pem'
  },
  */
  
  sessionSecret: 'some random str' // Use for express-session. generated by init. You don't need modify it.
};
```
## Start
`sudo node index.js`

linux-remote Can't start without root user identity, because the `login` shell cannot possibly work without effective root.


## Update
`cd /opt/linux-remote && npm update`

- `linux-remote-client` updated, you don't need restart server. Just need refresh browser.
- `@linux-remote/user-server` updated, you don't need restart server. Logined user need relogin.
- `linux-remote-server` updated, you need restart server.  All logined user force logout when you restart server.


## Donate
[patreon](https://www.patreon.com/hezedu): Du Wei is creating linux-remote

| Paypal | AliPay | WechatPay |
| ------------- | ------------- | ------------- |
| <a href="https://www.paypal.me/hezedu" target="_blank"><img src="https://www.paypalobjects.com/webstatic/paypalme/images/pp_logo_small.png" width="150"></a> | <img src="https://github.com/hezedu/SomethingBoring/blob/master/pay/alipay.png?raw=true&v=2" width="150"> | <img src="https://github.com/hezedu/SomethingBoring/blob/master/pay/wxpay.png?raw=true&v=2" width="150">


