
<div class = "wrapper pre">
  
</div>
<div class="wrapper">
  <div class="title">
    CSS Tabs
    <div class="line"></div>
  </div>
  <div class="container">
    <div class="card tabs">
      <input id="tab-1" type="radio" class="tab tab-selector" checked="checked" name="tab" />
      <label for="tab-1" class="tab tab-primary">Product</label>
      <input id="tab-2" type="radio" class="tab tab-selector" name="tab" />
      <label for="tab-2" class="tab tab-success">Options</label>
      <input id="tab-3" type="radio" class="tab tab-selector" name="tab" />
      <label for="tab-3" class="tab tab-default">Shipping</label>
      <input id="tab-4" type="radio" class="tab tab-selector" name="tab" />
      <label for="tab-4" class="tab tab-warning">Published</label>
      <div class="tabsShadow"></div>
      <div class="glider"></div>
      <section class="content">
        <div class="item" id="content-1">
          <h2 class="tab-title tab-primary">Sweep + Slide Dog Toy</h2>
          <p>
            <span class = "numit">1</span> The Sweep + Slide is an indoor dog toy with a sleek base designed to glide across any floor. Not only does this toy stimulate your dog's natural chase instincts, but it also sweeps away floor dust and grime with a replaceable sweeper bottom cover.
          </p>
        </div>
        <div class="item" id="content-2">
          <h2 class="tab-title tab-success">Tab 2</h2>
          <p>
            <span class = "numit">2</span> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor </p>
        </div>
        <div class="item" id="content-3">
          <h2 class="tab-title tab-default">Tab 3</h2>
          <p>
            <span class = "numit">3</span> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis </p>
        </div>
        <div class="item" id="content-4">
          <h2 class="tab-title tab-warning">Tab 4</h2>
          <p>
            <span class = "numit">4</span> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. </p>
        </div>
      </section>

    </div>
  </div>
</div>
/* Basic */
@import url("https://use.typekit.net/ovt6ynt.css");
@import url("https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;0,700;0,800;1,400;1,500;1,600;1,700;1,800&family=Oswald:wght@200;300;400;500;600;700&family=Roboto+Condensed:wght@300;400;700&family=Roboto:wght@100;300;400;500;700;900&family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700;1,900&family=Spectral:wght@200;300;400;500;600;700;800&display=swap");

body {
  padding: 0;
  margin: 0;
  height: 100%;
  font-family: "Roboto", sans-serif;
  background: linear-gradient(#141e30, #243b55);
}
.title {
  text-align: center;
  padding: 50px 0px 25px 0;
  font-size: 44px;
  font-weight: 600;
  color: #21222c;
  font-family: "Playfair Display SC";
}
.wrapper {
  background-color: #f6f8ff;
  width: 100%;
  min-height: 100vh;
  min-width: 90vh;
  background: transparent;
  opacity: 1;
}

.wrapper.pre {
  background-size: cover !important;
  background: url(https://images.unsplash.com/photo-1523633589114-88eaf4b4f1a8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3870&q=80);
  background: url(https://images.unsplash.com/photo-1462556791646-c201b8241a94?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2896&q=80);
  position: absolute;
  top: 0;
  z-index: -2;
  opacity: 0.75;
  background: url(https://assets.codepen.io/4927073/mybg.jpg);
}

.wrapper .line {
  width: 50%;
  margin: 25px auto 0 auto;
  height: 1px;
  background-color: #c3d2e3;
}

.container {
  width: 100%;
  padding: 10px 0;
  text-align: center;
  width: 90%;
  padding: 10px 0px;
  text-align: center;
  margin: auto;
}
.container .card {
  max-width: 600px;
  min-height: 140px;
  min-width: 595px;

  background-color: white;
  border-radius: 10px;
  border: 1px solid #e3e3e3;
  margin: 0 auto;
}
.tabs {
  text-align: left;
  position: relative;
}
.tabs input {
  position: absolute;
  opacity: 0;
  margin: 0;
  padding: 0;
}

.tabs input + label:hover {
  color: #777;
}
.tabs .tabsShadow {
  width: 100%;
  padding: 10px;
  box-shadow: 0 0 25px 0 rgba(0, 0, 0, 0.04);
  box-sizing: border-box;
  position: absolute;
  height: 35px;
  z-index: 0;
  top: 0;
  pointer-events: none;
}

.content .item {
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s;
  position: absolute;
  padding: 10px 20px;
}

#tab-1:checked ~ .glider {
  left: 0px;
}
#tab-2:checked + label {
  color: #51a14c;
}
#tab-2:checked ~ .glider {
  background: linear-gradient(90deg, #51a14c 0%, #10c33e 100%);
  box-shadow: 0px 0px 8px 0px rgba(47, 187, 12, 0.62);
}

#tab-3:checked + label {
  color: #525252;
}

#tab-1:checked ~ section #content-1,
#tab-2:checked ~ section #content-2,
#tab-3:checked ~ section #content-3,
#tab-4:checked ~ section #content-4 {
  opacity: 1;
  visibility: visible;
}

.tabs input + label {
  margin: 12px -8px;
  width: 15%;
  transition: all 0.3s;
  text-align: center;
  border: none;
  border-bottom: 0.5pt solid #1d1e22;
  color: #e7e9f5;
  display: inline-flex;
  -webkit-box-pack: center;
  padding: 5pt 10pt;
  vertical-align: top;
  justify-content: flex-start;
  background: #333;
  box-shadow: 1px 1px 2px 1px #231f20;
  text-transform: uppercase;
  font-weight: 300;
  font-size: 8pt;
  background: #26292c;
  margin-bottom: 0.5px;
  border-radius: 7px 7px 0 0 !important;
  border-top: 1px solid #3b3d3f;
  letter-spacing: 0.1666666667em !important;
  font-family: "antique-olive" !important;
  background: hsl(232deg 6% 17%);
  cursor: pointer;
}

.content {
  margin: 0px auto;
  text-align: left;
  line-height: 20px;
  height: 240px;
  border-radius: 5px;
  box-shadow: 0 2px 3px rgb(10 10 10 / 10%), 0 0 0 1px rgb(10 10 10 / 10%);
  display: block;
  padding: 1.25rem;
  z-index: 2;
  border-top: 1px solid #3b3d3f;
  background: hsl(232deg 16% 15%);
  position: relative;
}

.container .card {
  max-width: 600px;
  min-height: 140px;
  border-radius: 10px;
  border: none;
  margin: 0 auto;
  z-index: 4 !important;
  position: relative;
  background: linear-gradient(#141e30, #243b55);
  background: #16181a;
  border-top: 1px solid #3b3d3f;
  background: hsl(232deg 18% 8%);
}

.content p {
  margin: 10px 15px 10px 0;
  letter-spacing: 0.75px;
  font-size: 14pt;
  font-style: normal;
  color: #f0f2fc;
  line-height: 30px;
  margin-top: 10pt;
  font-family: "freight-display-pro";
  font-weight: 300 !important;
}
h2.tab-title.tab-warning,
h2.tab-title.tab-success,
h2.tab-title.tab-primary,
h2.tab-title.tab-default {
  display: inline-flex;
  color: #fff;
  background-position: bottom center;
  margin-bottom: 0pt !important;
  margin-top: 6pt;
  height: 22pt;
  text-fill-color: transparent !important;
  background-clip: text !important;
  -webkit-text-fill-color: transparent !important;
  -webkit-background-clip: text !important;
  -moz-background-clip: text;
  -moz-text-fill-color: transparent;
  -ms-background-clip: text;
  -ms-text-fill-color: transparent;
  text-transform: capitalize;
  font-size: 24px;
  letter-spacing: 0px;
  font-family: "Manrope" !important;
  font-weight: 800 !important;
}

h2.tab-title.tab-default {
  background: linear-gradient(10deg, #f7ec9c, #ff8651);
}

h2.tab-title.tab-success {
  background: linear-gradient(10deg, #02ce85, #02ceab);
}

h2.tab-title.tab-primary {
  background: linear-gradient(
    60deg,
    hsl(202deg 100% 75%),
    hsl(205deg 100% 64%),
    hsl(230deg 100% 75%),
    hsl(270deg 100% 72%)
  );
}

h2.tab-title.tab-warning {
  background: linear-gradient(70deg, #c51574, #97389b);
}

.tabs input {
  position: relative;
  opacity: 0;
  margin: auto !important;
  padding: 0;
}
label.tab.tab-primary {
  border-radius: 6pt 0 0 6pt;
}
label.tab.tab-warning {
  border-radius: 0 6pt 6pt 0;
}
#tab-1:checked + label {
  color: deepskyblue;
}
#tab-3:checked + label {
  color: #ffadfa;
  color: #ffaa75;
}
#tab-4:checked + label {
  color: #ffadfa;
}
#tab-1:checked ~ .glider {
  left: 1.6%;
}

#tab-2:checked ~ .glider {
  left: 21.85%;
}
#tab-3:checked ~ .glider {
  background: linear-gradient(
    90deg,
    #faffcc 0%,
    #f5eea3 10%,
    #ffe48a 40%,
    #ffb54d 65%,
    #ff974d 85%,
    #ff8052 100%
  );
  left: 42.15%;
  box-shadow: 0px 0px 8px 0px hsl(17.72deg 100% 70% / 70%);
}

#tab-4:checked ~ .glider {
  background: linear-gradient(90deg, #b9326f 0%, #ff5ddc 100%);
  box-shadow: 0px 0px 8px 0px rgba(231, 13, 93, 0.57);
  left: 62.365% !important;
}

.glider {
  width: 15%;
  padding: 0px 13px;
  height: 4.5px;
  border-radius: 0 0 1px 1px;
  position: absolute;
  box-shadow: 0px 0px 8px 0px hsl(262deg 100% 70% / 70%);
  background: linear-gradient(
    113deg,
    hsl(260deg 100% 64%) 0%,
    hsl(190deg 100% 55%) 100%
  );
  transition: all 0.3s;
  top: 36px;
  z-index: 2;
}

span.numit {
  font-size: 12pt;
  font-family: "muli";
  font-weight: 600;
  text-shadow: 0.5px 0.5px 0.5px #e7e9f5;
  color: #0e101a;
  margin-right: 2px;
  margin-left: -2px;
  padding: 0;
  color: aliceblue;
  text-shadow: 0.5pt 0.5pt 0.5pt #2d3748;
}
