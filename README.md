<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Banner - Guillermo Kissling</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        .banner {
            width: 100%;
            height: 300px;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 25%, #16213e 50%, #0f3460 75%, #1a1a2e 100%);
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-family: 'JetBrains Mono', 'Fira Code', 'Consolas', 'Monaco', 'Courier New', monospace;
        }

        .banner::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 80%, rgba(30, 144, 255, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 255, 255, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(70, 130, 180, 0.1) 0%, transparent 50%);
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .content {
            text-align: center;
            z-index: 2;
            position: relative;
        }

        .name {
            font-size: 3.5em;
            font-weight: 600;
            margin-bottom: 0.2em;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.7);
            animation: slideInFromTop 1s ease-out;
            letter-spacing: -0.02em;
        }

        .title {
            font-size: 1.4em;
            margin-bottom: 0.5em;
            opacity: 0.9;
            font-weight: 400;
            animation: slideInFromBottom 1s ease-out 0.3s both;
            letter-spacing: 0.02em;
        }

        .subtitle {
            font-size: 1.1em;
            opacity: 0.8;
            font-weight: 300;
            animation: slideInFromBottom 1s ease-out 0.6s both;
            letter-spacing: 0.05em;
        }

        @keyframes slideInFromTop {
            from {
                transform: translateY(-50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes slideInFromBottom {
            from {
                transform: translateY(30px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .code-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.1;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            line-height: 1.5;
            white-space: pre;
            overflow: hidden;
            z-index: 1;
            animation: scrollCode 20s linear infinite;
        }

        @keyframes scrollCode {
            0% { transform: translateY(0); }
            100% { transform: translateY(-50%); }
        }

        .tech-icons {
            position: absolute;
            top: 20px;
            right: 30px;
            display: flex;
            gap: 15px;
            z-index: 2;
        }

        .tech-icon {
            width: 40px;
            height: 40px;
            background: rgba(30, 144, 255, 0.15);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            backdrop-filter: blur(10px);
            animation: bounce 2s infinite;
        }

        .tech-icon:nth-child(1) { animation-delay: 0s; }
        .tech-icon:nth-child(2) { animation-delay: 0.2s; }
        .tech-icon:nth-child(3) { animation-delay: 0.4s; }
        .tech-icon:nth-child(4) { animation-delay: 0.6s; }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .location {
            position: absolute;
            bottom: 20px;
            left: 30px;
            font-size: 0.9em;
            opacity: 0.8;
            z-index: 2;
        }

        @media (max-width: 768px) {
            .banner {
                height: 200px;
            }
            
            .name {
                font-size: 2.5em;
            }
            
            .title {
                font-size: 1.2em;
            }
            
            .subtitle {
                font-size: 1em;
            }
            
            .tech-icons {
                top: 15px;
                right: 20px;
                gap: 10px;
            }
            
            .tech-icon {
                width: 30px;
                height: 30px;
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <div class="banner">
        <div class="code-bg">
def optimize_web_performance():
    """Optimizing Core Web Vitals"""
    page_speed = improve_lcp()
    cls_score = reduce_layout_shift()
    return f"PageSpeed: {page_speed} | CLS: {cls_score}"

class FullStackDeveloper:
    def __init__(self):
        self.name = "Guillermo Kissling"
        self.stack = ["Python", "Flask", "React", "Docker"]
        self.experience = "4+ years"
        self.specialties = ["Web Performance", "SEO", "E-commerce"]
    
    def current_focus(self):
        return "Building scalable web solutions"

# Docker deployment
FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python", "app.py"]

// React Component
const WebOptimizer = () => {
  const [performance, setPerformance] = useState(85);
  
  useEffect(() => {
    optimizeImages();
    implementLazyLoading();
    minimizeJSBundle();
  }, []);

  return (
    &lt;div className="performance-dashboard"&gt;
      &lt;h2&gt;PageSpeed Score: {performance}&lt;/h2&gt;
    &lt;/div&gt;
  );
};

// MySQL optimization
SELECT p.*, c.name as category
FROM products p
LEFT JOIN categories c ON p.category_id = c.id
WHERE p.active = 1
ORDER BY p.created_at DESC
LIMIT 20;

# Flask E-commerce API
@app.route('/api/products', methods=['GET'])
def get_products():
    page = request.args.get('page', 1, type=int)
    products = Product.query.paginate(
        page=page, per_page=10, error_out=False
    )
    return jsonify({
        'products': [p.to_dict() for p in products.items],
        'total': products.total
    })

def optimize_web_performance():
    """Optimizing Core Web Vitals"""
    page_speed = improve_lcp()
    cls_score = reduce_layout_shift()
    return f"PageSpeed: {page_speed} | CLS: {cls_score}"
        </div>
        
        <div class="tech-icons">
            <div class="tech-icon">🐍</div>
            <div class="tech-icon">⚛️</div>
            <div class="tech-icon">🐳</div>
            <div class="tech-icon">🚀</div>
        </div>
        
        <div class="content">
            <h1 class="name">Guillermo Kissling</h1>
            <p class="title">Mid Full Stack Developer</p>
            <p class="subtitle">Python & Web Performance Specialist</p>
        </div>
        
        <div class="location">📍 Málaga, España</div>
    </div>
</body>
</html>

<h1 align="center">👋 ¡Hola! Soy Guillermo Kissling</h1>
<h3 align="center">Mid Full Stack Developer | Python & Web Performance Specialist</h3>

<div align="center">
  <a href="https://linkedin.com/in/dkkissling">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:danielkissling65@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>
  <a href="https://github.com/DkKissling?tab=repositories">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=github&logoColor=white" alt="Portfolio">
  </a>
</div>

---

## 🚀 Sobre Mí

*4+ años de experiencia* desarrollando soluciones Full Stack con enfoque en *Python y optimización web*. 

💡 *Destacados:*
- Optimicé Core Web Vitals (LCP/CLS) para sitio con *10K visitas diarias*
- Mejorando PageSpeed de *45 a 85+* y reduciendo tiempos de carga en *40%*
- Migré sistemas legacy manejando *+3K transacciones diarias*
- Dockerización de aplicaciones y desarrollo de e-commerce con pasarelas de pago

🎯 *Especializado en:* Python/Flask, Docker, SEO técnico, Computer Vision y migración de sistemas legacy

---

## 💼 Experiencia Reciente

### 🔹 Autónomo | Full Stack Developer (Mar 2024 - Actualidad)
- Desarrollo de soluciones e-commerce con *Python/Flask y Docker*
- Implementación de pasarela de pagos con *Mercado Pago*
- Diseño de modelos relacionales escalables (*MySQL*)
- Colaboración frontend con *React/Tailwind CSS*

### 🔹 TopTive | Frontend Developer & SEO Specialist (Jul 2021 - Jul 2023)
- Optimización SEO técnico con *Ezoic*
- Desarrollo con *Next.js* y *Tailwind CSS*
- Implementación de *lazy loading* y optimización de assets
- Diagnóstico y corrección de errores JavaScript en producción

---

## 🛠️ Stack Tecnológico

<div align="center">
  <table>
    <tr>
      <td width="50%">
        <h3>🔧 Tecnologías Principales</h3>
        <p align="center">
          <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
          <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
          <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
          <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React">
          <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js">
          <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
          <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
          <img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
          <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
          <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">
        </p>
        <h3>🎨 Frontend & Styling</h3>
        <p align="center">
          <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
          <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
          <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind">
          <img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap">
        </p>
        <h3>☁️ DevOps & Cloud</h3>
        <p align="center">
          <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS">
          <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
          <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions">
        </p>
      </td>
      <td width="50%">
        <div align="center">
          <img src="https://raw.githubusercontent.com/AVS1508/AVS1508/master/assets/Night-Coding.gif" alt="Night Coding" width="100%">
        </div>
      </td>
    </tr>
  </table>
</div>

---

## ⭐ Proyectos Destacados

<div align="center">
  <table>
    <tr>
      <th>Proyecto</th>
      <th>Descripción</th>
      <th>Tecnologías</th>
      <th>Logros</th>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/DkKissling/Clothing-Store-Flask">🛍️ Clothing Store E-commerce</a></strong></td>
      <td>Sistema completo con panel admin y pasarela de pagos</td>
      <td>Python, Flask, Docker, JWT, MySQL</td>
      <td>Sistema completo con pagos automáticos</td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/DkKissling/facial-recognition">👁️ Facial Recognition System</a></strong></td>
      <td>Detección y reconocimiento facial en tiempo real</td>
      <td>Python, OpenCV, Face Recognition</td>
      <td>Procesamiento en tiempo real optimizado</td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/DkKissling/flask-Docker-Blog">📝 Blog with Auth</a></strong></td>
      <td>CRUD con autenticación JWT y PostgreSQL</td>
      <td>Python, Docker, PostgreSQL, JWT</td>
      <td>Reducción 70% tiempo configuración</td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/DkKissling/Library-Management-System">📚 Library Management</a></strong></td>
      <td>Sistema automatizado de préstamos con cálculo de multas</td>
      <td>Java, MySQL, Hibernate</td>
      <td>Eliminó 90% de errores manuales</td>
    </tr>
  </table>
</div>

---

## 🏆 Logros Técnicos

- 🚀 *Optimización Web:* PageSpeed 45 → 85+ | Core Web Vitals mejorados
- 📈 *Performance:* Reducción 40% tiempo de carga | 10K visitas diarias
- 🔄 *Migración:* Sistemas legacy con +3K transacciones diarias
- 🎯 *Eficiencia:* Mejora 35% en consultas SQL | 25% usabilidad frontend
- 🐳 *DevOps:* Dockerización completa | CI/CD con GitHub Actions

---

## 🎓 Certificaciones

- 🐍 *Python TOTAL* - Udemy.inc - Programador Avanzado (2024-2025)
- 💻 *Full Stack Development* - University of Helsinki (2023-2024)
- ⚛️ *Frontend Developer Libraries* - FreeCodeCamp (2023-2024)
- 🎯 *Desarrollo de Software* - ITEC Río Cuarto (2020-2023)

---

## 📫 Contacto

<div align="center">
  <table>
    <tr>
      <td>
        <img src="https://img.shields.io/badge/Email-danielkissling65@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
      </td>
      <td>
        <img src="https://img.shields.io/badge/LinkedIn-dkkissling-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
      </td>
      <td>
        <img src="https://img.shields.io/badge/Location-Málaga,_España-FF5722?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location">
      </td>
    </tr>
  </table>
</div>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=DkKissling&style=for-the-badge&color=0e75b6" alt="Profile Views">
  <img src="https://img.shields.io/github/followers/DkKissling?style=for-the-badge&color=0e75b6" alt="GitHub Followers">
</div>

<div align="center">
  <i>⚡ "Optimizando código y mejorando experiencias web, un commit a la vez" ⚡</i>
</div>
