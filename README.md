<!DOCTYPE html>

<head>
  <title>กำลังเข้าสู่ Form</title>
  <style>
    .centerScreen {
      margin-top: 20;
      margin-right: auto;
      margin-bottom: 20;
      margin-left: auto;
    }
  </style>
</head>

<body style="background-color: powderblue;">
  <div class="centerScreen">
    <center>
      <img src="https://drive.google.com/uc?id=1mEyShWSX9rPf4klIDeMTlHAOc4BsySFK" height="200px" , width="200px" />
      <h1>
        กำลังเข้าสู่ Google Form กรุณารอซักครู่
      </h1>
    </center>
  </div>
</body>
<footer>
  <script src="https://static.line-scdn.net/liff/edge/2.1/sdk.js"></script>
  <script>

    const liffId = "1657358045-dG68K4Bv";

    liff.ready
      .then(() => {
        if (liff.isLoggedIn()) {
          return liff.getProfile();
        } else {
          liff.login({
            redirectUri: "xxxxxxxxx",
          });
        }
      })
      .then((profile) => {
        window.location.replace(
          `https://docs.google.com/forms/d/e/1FAIpQLScd5HJw41htuMDVSSXTCrSIygcKs0Y76SUQ0T88z_2L1fWWqA/viewform?usp=pp_url&entry.1883626392=${profile.userId}&entry.39038656=${profile.displayName}&entry.1850014025=${profile.pictureUrl}&entry.553353270=${profile.statusMessage}`
        );
      });

 
    liff.init(
      {
        liffId: liffId,
      },
      () => {},
      (err) => {
        window.alert(err);
      }
    );
  </script>
</footer>

