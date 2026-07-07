<template>

<footer id="contact" class="footer">
    <div class="footer-content">
        <div class="footer-brand">
            <h1>AKARA</h1>
            <p>
                LOCAL CRAFTSMANSHIP<br>WORLD CLASS COMFORT
            </p>
            <div class="contact-info">
                <p>📍 Kediri, Indonesia</p>
                <p>📧 hello@akara.id</p>
                <p>📞 +62 000 0000 0000</p>
            </div>
        </div>
        <div class="footer-links">
            <h3>Explore</h3>
            <a href="#home">Home</a>
            <a href="#collection">Collection</a>
            <a href="#artisans">Artisans</a>
            <a href="#contact">Contact</a>
        </div>
        <div class="footer-social">
            <h3>Follow Us</h3>
            <a href="">Instagram</a>
            <a href="">Facebook</a>
            <a href="">Pinterest</a>
            <a href="">LinkedIn</a>
        </div>
    </div>
    <div class="footer-line"></div>
    <div class="footer-bottom">
        <p>
             © 2026 AKARA. All Rights Reserved.
        </p>
        <p>
            Designed with Indonesian Craftsmanship.
        </p>
    </div>
</footer>
</template>

<style scoped>
.footer{
    background:#2F2A26;
    padding:80px 90px 40px;
}
.footer-content{
    display:flex;
    justify-content:space-between;
    gap:100px;
}
.footer-brand{
    flex:2;
}
.footer-brand h1{
    font-family:"Cormorant Garamond",serif;
    color:#F8F5F1;
    font-size:54px;
    margin-bottom:20px;
}
.footer-brand p{
    color:#D7CEC2;
    line-height:1.8;
}
.contact-info{
    margin-top:35px;
}
.contact-info p{
    margin:10px 0;
}
.footer-links,
.footer-social{
    display:flex;
    flex-direction:column;
    gap:14px;
}

.footer-links h3,.footer-social h3{
    color:#C9A86A;
    margin-bottom:10px;
    font-family:Inter,sans-serif;
}
.footer-links a,.footer-social a{
    color:#F8F5F1;
    text-decoration:none;
    transition:.25s;
}
.footer-links a:hover,.footer-social a:hover{
    color:#C9A86A;
}
.footer-line{
    height:1px;
    background:#4D4743;
    margin:55px 0 30px;
}
.footer-bottom{
    display:flex;
    justify-content:space-between;
    color:#A89F94;
    font-size:14px;
}

@media(max-width:900px){
.footer-content{
    flex-direction:column;
    gap:45px;
}

.footer-bottom{
    flex-direction:column;
    gap:10px;
}

.footer{
    padding:60px 30px;

}
}

</style>