 <script>
    let btn1 = document.querySelector('#box1  a')
    let btn2 = document.querySelector('#box2  a')
    let btn3 = document.querySelector('#box3  a')
    let btn4 = document.querySelector('#box4  a')
    let btn5 = document.querySelector('#box5  a')
    let btn6 = document.querySelector('#box6  a')
    let msgbtn = document.querySelector('.message-bar')
    let sliderimg = document.querySelector('#slider-img')
    let leftbtn = document.querySelector('#left')
    let rightbtn = document.querySelector('#right')
    let dots = Array.from(document.querySelectorAll('.dot'))
    let active =document.querySelector('.active');
    let arrowup =document.querySelector('#arrow');
    let onsale =document.querySelector('#fire');
    let catagories =document.querySelector('#catagories-img');
    let person_1 =document.querySelector('#person1');
    let person_2 =document.querySelector('#person2');
  
    // ============================================================ 
    let sliderarr = Array.from([
      { imgpath: './front-slider/1stimg.jpg' },
      { imgpath: './front-slider/frontimg2.jpg' },
      { imgpath: './front-slider/frontimg3.jpg' },
      { imgpath: './front-slider/frontimg4.jpg' },
      { imgpath: './front-slider/frontimg5.jpg' },
      { imgpath: './front-slider/frontimg6.jpg' },
      { imgpath: './front-slider/frontimg7.jpg' },
      { imgpath: './front-slider/frontimg8.jpg' },
      { imgpath: './front-slider/frontimg9.jpg' },
      { imgpath: './front-slider/frontimg10.jpg' },
      { imgpath: './front-slider/frontimg11.jpg' },
      { imgpath: './front-slider/frontimg12.jpg' },
      { imgpath: './front-slider/frontimg13.jpg' },
      { imgpath: './front-slider/frontimg14.jpg' },
      { imgpath: './front-slider/frontimg15.jpg' },
    ])
    let currimg = 0
    // ====================================================
    btn4.addEventListener('click', () => {
      func1()

    })
    let func1 = () => {
      let div = document.createElement("div");
      let login = document.querySelector(".login");
      div.classList.toggle("login");
      div.innerHTML = `
        <div class="login-page">
            <div id="part1">
                <p>Password</p>
                <p>Phone Number</p>
                <img src="./logos/close.png" alt="loading" id="close">
            </div>
            <div id="part2">
                <input type="email" placeholder="Please enter your Phone Number or Email" id="email" />
                <input type="password" placeholder="Please enter your Password" id="password" />
                <p>Forget Password?</p>
                <button>LOG IN</button>
            </div>
            <div id="part3">
                <p>Don't have an account?<span>Sign up</span></p>
                <p>Or, login with </p>
               <div id="logos-box"> <img src="./logos/facebooklogo.png" alt="loading" id="facebooklogo"><p>Facebook</p>
                <img src="./logos/googlelogo.png" alt="loading" id="googlelogo"><p>Google</p>
            </div>
            </div>
        </div>
 
  `
      document.body.appendChild(div);
      let close1 = document.querySelector('#close');
      close1.addEventListener('click', () => {

        document.body.removeChild(div);
      })

    }
    // ====================================================== 
    btn5.addEventListener('click', () => {
      func2()
    })
    let func2 = () => {
      let div = document.createElement("div");
      let login = document.querySelector(".login");
      div.classList.toggle("login");
      div.innerHTML = `
       <div class="login-page  signup-page">
            <div id="part1" class="part1-signup">
                <p>Sign up</p>
                <img src="./logos/close.png" alt="loading" id="close">
            </div>
            <div id="part2" class="part2-signup">
                <div id="input-box">
                    <p>PK+92</p>
                <input type="text" placeholder="Please enter your Phone Number" id="number" />
               <div id="checkbox-box"> <input type="checkbox"  id="checkbox" /><span id="checkbox-text">By creating and/or using your account, you agree to our <span>Terms of Use</span>  and <span>Privacy Policy</span>.</span></div>
            </div>
                <button id="send"><img src="./logos/whatsaplogo.svg" alt="loading" id="whatsapp-logo">Send code via Whatsapp</button>
            </div>
            <div id="part3">
                <p>Don't have an account?<span>Log in Now</span></p>
                <p>Or, login with </p>
               <div id="logos-box"> <img src="./logos/facebooklogo.png" alt="loading" id="facebooklogo"><p>Facebook</p>
                <img src="./logos/googlelogo.png" alt="loading" id="googlelogo"><p>Google</p>
               </div>
 
  `
      document.body.appendChild(div);
      let close1 = document.querySelector('#close');
      close1.addEventListener('click', () => {
        document.body.removeChild(div);
      })

    }
    // ========================================================== 
    btn1.addEventListener('click', () => {
      func3()
    })
    let func3 = () => {
      let download = document.querySelector(".app-download");
      if (download) {
        // If the app-download section already exists, remove it
        download.remove();
      } else {
        // Create and append it if it doesn't exist
        let div = document.createElement("div");
        div.classList.add("app-download");
        div.innerHTML = `
            <p>Download the App</p>
            <img src="./logos/qrcode.avif" alt="loading" id="qr-code2">
            <div class="links">
                <img src="./logos/appstorelogo.png" alt="loading" class="apps-logos">
                <img src="./logos/playstorelogo.png" alt="loading" class="apps-logos">
            </div>
        `;
        document.body.appendChild(div);
      }
    };
    // ===========================================================
    btn3.addEventListener('click', () => {
      func4()
    })
    let func4 = () => {
      let class1 = document.querySelector(".help-bar");
      if (class1) {
        // If the app-download section already exists, remove it
        class1.remove();
      } else {
        // Create and append it if it doesn't exist
        let div = document.createElement("div");
        div.classList.add("help-bar");
        div.innerHTML = `
        <div class="options">
            <img src="./logos/help-center-logo.png" alt="loading" class="help-logos"><span class="help-text">Help Center</span>
        </div>
        <div class="options">
            <img src="./logos/calllogo.png" alt="loading" class="help-logos"><span class="help-text">Contact Customer Care</span>
        </div>
        <div class="options">
            <img src="./logos/orderlogo.png" alt="loading" class="help-logos"><span class="help-text">Order</span>
        </div>
        <div class="options">
            <img src="./logos/shiplogo.png" alt="loading" class="help-logos"><span class="help-text">Shipping & Delivery</span>
        </div>
        <div class="options">
            <img src="./logos/paymentlogo.png" alt="loading" class="help-logos"><span class="help-text">Payment</span>
        </div>
        <div class="options">
            <img src="./logos/refundlogo.png" alt="loading" class="help-logos"><span class="help-text">Returns & Refunds</span>
        </div>
        `;
        document.body.appendChild(div);
      }
    };
    // ================================================================== 
    btn6.addEventListener('click', () => {
      func5()
    })
    let func5 = () => {
      let class1 = document.querySelector(".language");
      if (class1) {
        // If the app-download section already exists, remove it
        class1.remove();
      } else {
        // Create and append it if it doesn't exist
        let div = document.createElement("div");
        div.classList.add("language");
        div.innerHTML = `
        <div class="urdu-box">
             <img src="./logos/paklogo.png" alt="loading" class="lang-logo">
             <span>Urdu</span>
            <input type="radio" id="urdu" name="language">
        </div>
        <div class="english-box">
            <img src="./logos/englogo.png" alt="loading" class="lang-logo">
            <span>English</span>
            <input type="radio" id="english" name="language">
        </div>
    </div>
        `;
        document.body.appendChild(div);
      }
    };
    // ======================================================================== 
    msgbtn.addEventListener('click', () => {
      messagefunc()
    })
    let messagefunc = () => {
      let class1 = document.querySelector(".message");
      if (class1) {
        class1.remove();
      } else {
        let div = document.createElement("div");
        div.classList.add("message");
        div.innerHTML = `
        <div class="msg-part-1">
            <div id="msg-bar-show">
                <img src="./logos/message logo.png" alt="loading" id="msg-logo">
                <span>Message</span>
            </div>
            <div id="msg-space"></div>
        </div>
        <div class="msg-part-2">
            <p id="name">Draze</p>
            <div id="msg-content">
                <img src="./logos/msg-logo-2.png" alt="loading" id="msg-logo-2">
                <div id="msg-about">
                    <p id="blue">Use the App for exclusive offers!</p>
                    <p>Once you start a new conversation, you’ll see it listed here.</p>
                    <div id="option1">
                        <span class="option">login</span> <span>/</span>
                        <span class="option">Sign up</span>
                    </div>
                </div>
            </div>
        </div>
        `;
        document.body.appendChild(div);
      }
    };
    // =============================================================================== 
    let sliderfunc = () => {
      sliderarr.forEach((e, i) => {
        if (i === currimg) {
          sliderimg.setAttribute('src', sliderarr[i].imgpath);
        }
      });
      dots.forEach((e, i) => {
        e.classList.remove('active');
        if (i === currimg) {
          e.classList.add('active');
        }
      });
    };
    sliderfunc();
    if (leftbtn) {
      leftbtn.addEventListener('click', () => {
        currimg = (currimg - 1 + sliderarr.length) % sliderarr.length;
        sliderfunc();
      });
    }
    if (rightbtn) {
      rightbtn.addEventListener('click', () => {
        currimg = (currimg + 1) % sliderarr.length;
        sliderfunc();
      });
    }
    setInterval(() => {
      currimg = (currimg + 1) % sliderarr.length;
      sliderfunc();
    }, 4000);
// ================================================================================== 
arrowup.addEventListener('click', () => {
  window.scrollTo({top: 0, behavior:'smooth'});
  
})
onsale.addEventListener('click', () => {
  window.scrollTo({top: 500, behavior:'smooth'});
  
})
catagories.addEventListener('click', () => {
  window.scrollTo({top: 850, behavior:'smooth'});
  
})
person_1.addEventListener('click', () => {
  window.scrollTo({top: 1270 , behavior:'smooth'});
  
})
person_2.addEventListener('click', () => {
  window.scrollTo({top: 1270 , behavior:'smooth'});
  
})
