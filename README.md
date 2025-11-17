# Generador de Estrategias de Negocio Inteligente con IA

## 💡 Descripción del Proyecto

Este proyecto es una plataforma web desarrollada en Django que funciona como un **Generador de Estrategias de Negocio Inteligente**, diseñado específicamente para pequeñas y medianas empresas (PYMES). La aplicación recibe información clave del negocio (sector, tamaño, recursos y descripción) y utiliza técnicas de Procesamiento de Lenguaje Natural (PLN) y un motor de reglas interno para generar estrategias de negocio personalizadas (marketing, ventas, operaciones o digital).

El objetivo es democratizar la planificación estratégica, proporcionando un borrador de plan de acción basado en análisis de datos básicos y lógica de negocio.

## ✨ Características Principales

* **Generación Personalizada:** Produce estrategias adaptadas al sector y los recursos disponibles de la empresa.
* **Análisis con PLN:** Emplea las librerías **NLTK** y **SpaCy** para extraer palabras clave y realizar un análisis de "sentimiento" (básico), ajustando las recomendaciones estratégicas.
* **Motor de Reglas:** Lógica interna robusta que define estrategias específicas para diferentes escenarios y verticales de negocio.
* **Gestión de Datos:** Utiliza Django para manejar la persistencia de las estrategias generadas en una base de datos.
* **Interfaz Simple:** Interfaz de usuario intuitiva renderizada directamente con plantillas de Django (HTML/CSS/JS).
* **Integridad y SEO:** Incluye validaciones en backend y frontend, además de configuración básica de SEO (sitemaps).
* **Seeder de Datos:** Comando de gestión de Django para poblar rápidamente la base de datos con información de ejemplo.

## 🛠️ Tecnologías Utilizadas

| Categoría | Tecnología | Propósito |
| :--- | :--- | :--- |
| **Backend** | Python | Lenguaje principal de programación. |
| **Framework** | Django | Marco de desarrollo web robusto y seguro. |
| **PLN** | NLTK & SpaCy | Procesamiento de texto, extracción de entidades y análisis básico de contexto. |
| **Base de Datos** | SQLite3 | Base de datos por defecto para el desarrollo. |

## ⚙️ Configuración y Ejecución

Sigue estos pasos para poner en marcha el proyecto:

### Requisitos

* Python 3.8+
* pip

### 1. Clonar el Repositorio

```bash
git clone [https://github.com/santiagourdaneta/Generador-de-Estrategias-de-Negocio-con-IA-Python-Django-LTK-SpaCy](https://github.com/santiagourdaneta/Generador-de-Estrategias-de-Negocio-con-IA-Python-Django-LTK-SpaCy)
cd Generador-de-Estrategias-de-Negocio-con-IA-Python-Django-LTK-SpaCy

2. Configuración del Entorno

# Crear entorno virtual
python -m venv venv

# Activar entorno virtual
# En Windows: .\venv\Scripts\activate
# En macOS/Linux: source venv/bin/activate

# Instalar dependencias
pip install -r requirements.txt

3. Descargar Modelos de PLN
Es necesario descargar los modelos lingüísticos para NLTK y SpaCy:

python -m spacy download es_core_news_sm
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords')"

4. Base de Datos y Superusuario

# Realizar migraciones
python manage.py makemigrations
python manage.py migrate

# (Opcional) Crear superusuario para el Admin de Django
python manage.py createsuperuser

# (Opcional) Poblar con datos de ejemplo
python manage.py seed_db

5. Iniciar el Servidor

python manage.py runserver

El servidor estará disponible en http://127.0.0.1:8000/.

⏭️ Próximos Pasos (Roadmap)

Integración con modelos de lenguaje grandes (LLMs) como Gemini para estrategias más sofisticadas.
Implementación de autenticación de usuarios.
Funcionalidad de exportación de estrategias a PDF/DOCX.
Mejoras en la experiencia del usuario (UX/UI) del dashboard.

