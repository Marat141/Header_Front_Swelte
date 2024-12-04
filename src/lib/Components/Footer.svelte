<footer>
    <h1>Foolish developer</h1>
    <p>Foolish developer is a blog website where you will find great tutorials on web design and development.</p>
    <div class="links">
        <a href="/"><img src="/" alt=""></a>
        <a href="/"><img src="/" alt=""></a>
        <a href="/"><img src="/" alt=""></a>
        <a href="/"><img src="/" alt=""></a>
        <a href="/"><img src="/" alt=""></a>   
    </div>
    <div class="second-footer">
        <h3>Copyright 2021</h3>
        <div class="main-links">
            <a href="/">Home</a>
            <a href="/Login">Login</a>
            <a href="/Register">Register</a>
        </div>
    </div>
</footer>

<style lang="scss">
    footer {
      background-color: #111; /* Černé pozadí */
      color: #fff;           /* Bílé písmo */
      text-align: center;    /* Vycentrovaný text */
      padding: 20px 0;
      margin-bottom: 0;
    
      h1 {
        font-size: 2rem;
        margin-bottom: 10px;
      }
    
      p {
        font-size: 1rem;
        margin-bottom: 20px;
        color: #ccc; /* Světle šedé písmo */
      }
    
      .links {
        display: flex;
        justify-content: center;
        gap: 15px; /* Mezera mezi ikonami */
    
        a {
          img {
            width: 30px;
            height: 30px;
            border-radius: 50%; /* Kulaté ikony */
            background-color: #444; /* Šedé pozadí */
            padding: 5px;
    
            &:hover {
              background-color: #666; /* Hover efekt */
            }
          }
        }
      }
    
      .second-footer {
        margin-top: 30px;
        border-top: 1px solid #333; /* Oddělující čára */
        padding-top: 15px;
    
        h3 {
          font-size: 1rem;
          margin-bottom: 10px;
        }
    
        .main-links {
          display: flex;
          justify-content: center;
          gap: 15px; /* Mezera mezi odkazy */
    
          a {
            font-size: 0.9rem;
            color: #fff;
            text-decoration: none;
            transition: color 0.3s;
    
            &:hover {
              color: #ccc; /* Hover efekt na odkazech */
            }
          }
        }
      }
    
      /* Responzivita */
      @media (max-width: 768px) { /* Tablety */
        h1 {
          font-size: 1.5rem;
        }
    
        p {
          font-size: 0.9rem;
        }
    
        .links a img {
          width: 25px;
          height: 25px;
        }
    
        .main-links {
          gap: 10px; /* Menší mezery mezi odkazy */
        }
      }
    
      @media (max-width: 480px) { /* Telefony */
        padding: 15px 10px;
    
        h1 {
          font-size: 1.2rem;
        }
    
        p {
          font-size: 0.8rem;
        }
    
        .links {
          flex-wrap: wrap; /* Ikony na další řádek, pokud je málo místa */
          gap: 10px;
    
          a img {
            width: 20px;
            height: 20px;
          }
        }
    
        .second-footer {
          h3 {
            font-size: 0.9rem;
          }
    
          .main-links {
            flex-wrap: wrap; /* Odkazy na další řádek, pokud se nevejdou */
            gap: 5px;
    
            a {
              font-size: 0.8rem;
            }
          }
        }
      }
    }
</style>