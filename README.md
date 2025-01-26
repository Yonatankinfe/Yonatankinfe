<!-- Add CSS animations and styling -->
<style>
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  @keyframes iconHover {
    0% { transform: translateY(0); }
    50% { transform: translateY(-5px); }
    100% { transform: translateY(0); }
  }
  
  .profile-title {
    animation: fadeIn 1.5s ease-out;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #2f3542;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
    border-bottom: 3px solid #70a1ff;
    display: inline-block;
    padding-bottom: 5px;
  }
  
  .tech-icons img {
    transition: all 0.3s ease-in-out;
    filter: grayscale(30%);
    margin: 8px;
    padding: 8px;
    background: rgba(255,255,255,0.9);
    border-radius: 50%;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  }
  
  .tech-icons img:hover {
    animation: iconHover 0.8s ease-in-out infinite;
    filter: grayscale(0%);
    transform: scale(1.15);
    box-shadow: 0 8px 12px rgba(0,0,0,0.2);
  }
  
  .social-badge {
    transition: all 0.3s ease;
    border-radius: 25px;
    overflow: hidden;
    position: relative;
    margin: 10px 5px;
  }
  
  .social-badge:hover {
    transform: scale(1.08);
    box-shadow: 0 6px 12px rgba(0,0,0,0.15);
  }
  
  .social-badge::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(
      90deg,
      transparent,
      rgba(255,255,255,0.4),
      transparent
    );
    transition: 0.5s;
  }
  
  .social-badge:hover::before {
    left: 100%;
  }
  
  body {
    background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
    padding: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
  }
  
  .profile-section {
    background: rgba(255,255,255,0.95);
    padding: 2rem;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    backdrop-filter: blur(10px);
    margin: 20px 0;
    max-width: 800px;
    width: 100%;
  }
</style>

<div class="profile-section">
  <h1 class="profile-title">👋 Hello there! I'm Yonatan Kinfe</h1>
  <h3 style="color: #57606f; margin-top: 10px;">🚀 Full-Stack Developer | 💻 Computer Engineer</h3>
  
  <p style="font-size: 1.1em; color: #2f3542; line-height: 1.6; margin: 20px 0;">
    Passionate about crafting robust solutions and beautiful user experiences. 
    Turning coffee into code since [your starting year]! ☕️
  </p>

  <div class="tech-icons" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin: 30px 0;">
    <img title="Kubernetes" alt="Kubernetes" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-plain-wordmark.svg" />
    <img title="Docker" alt="Docker" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg" />
    <img title="AWS" alt="AWS" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" />
    <img title="Python" alt="Python" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original-wordmark.svg" />
    <img title="Flask" alt="Flask" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original-wordmark.svg" />
    <img title="Java" alt="Java" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg" />
    <img title="Spring" alt="Spring" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-plain-wordmark.svg" />
    <img title="JavaScript" alt="JavaScript" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" />
    <img title="TypeScript" alt="TypeScript" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" />
    <img title="React" alt="React" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original-wordmark.svg" />
    <img title="Jest" alt="Jest" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jest/jest-plain.svg" />
    <img title="HTML5" alt="HTML5" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original-wordmark.svg" />
    <img title="CSS3" alt="CSS3" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original-wordmark.svg" />
  </div>

  <div style="text-align: center; margin-top: 30px;">
    <h3 style="color: #2f3542; margin-bottom: 15px;">📫 Let's Connect!</h3>
    <div style="display: flex; justify-content: center; gap: 20px;">
      <a class="social-badge" href="mailto:yonatankinfe0@gmail.com" target="_blank">
        <img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
      </a>
      <a class="social-badge" href="https://www.linkedin.com/in/yonatan-kinfe-7392a1274" target="_blank">
        <img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
      </a>
    </div>
  </div>
</div>