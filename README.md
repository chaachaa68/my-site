# my-site
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Chaachaa - Arduino Projects</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #f4f4f4; color: #333; }
    header { background: #007acc; color: white; padding: 1rem 2rem; text-align: center; }
    nav { text-align: center; margin: 15px 0; }
    nav button {
      background: #007acc; border: none; color: white; padding: 10px 15px;
      margin: 0 5px; cursor: pointer; border-radius: 4px;
    }
    section {
      max-width: 900px; margin: auto; background: white; padding: 20px;
      border-radius: 8px; margin-bottom: 20px;
    }
    footer { text-align: center; padding: 15px; background: #222; color: white; }
  </style>
</head>
<body>
  <header>
    <h1>Chaachaa - Arduino Projects</h1>
  </header>

  <nav>
    <button onclick="setLang('en')">English</button>
    <button onclick="setLang('ar')">العربية</button>
    <button onclick="setLang('fr')">Français</button>
  </nav>

  <section id="content"></section>

  <footer>
    &copy; 2025 Chaachaa
  </footer>

  <script>
    const data = {
      en: {
        title: "Welcome to Chaachaa's Arduino Projects",
        intro: "Arduino is an open-source electronics platform...",
        projectTitle: "My 2WD Arduino Robot Project",
        projectDesc: "A 2-wheel robot using Arduino Uno and L298N motor driver.",
        about: "About Chaachaa",
        aboutDesc: "Chaachaa is passionate about robotics and electronics."
      },
      ar: {
        title: "مرحبًا بك في مشاريع شاشة",
        intro: "Arduino منصة إلكترونية مفتوحة وسهلة الاستخدام...",
        projectTitle: "مشروعي: روبوت بعجلتين",
        projectDesc: "روبوت بعجلتين يستخدم Arduino Uno و L298N.",
        about: "عن شاشة",
        aboutDesc: "شغوف بالإلكترونيات والروبوتات."
      },
      fr: {
        title: "Bienvenue sur les projets Arduino de Chaachaa",
        intro: "Arduino est une plateforme open-source facile à utiliser...",
        projectTitle: "Mon robot 2 roues Arduino",
        projectDesc: "Robot à 2 roues avec Arduino Uno et L298N.",
        about: "À propos de Chaachaa",
        aboutDesc: "Chaachaa aime l'électronique et la robotique."
      }
    };

    function setLang(lang) {
      const c = data[lang];
      document.getElementById('content').innerHTML = `
        <h2>${c.title}</h2><p>${c.intro}</p>
        <h3>${c.projectTitle}</h3><p>${c.projectDesc}</p>
        <h3>${c.about}</h3><p>${c.aboutDesc}</p>`;
      document.body.dir = (lang === 'ar') ? 'rtl' : 'ltr';
    }

    setLang('en');
  </script>
</body>
</html>
