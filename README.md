# ontologia-recomendador
ACTIVIDAD 9. USO DE ONTOLOGÍA CON AGENTE 
# Ontología de Ciberseguridad

## Descripción

Este proyecto consiste en el desarrollo de una ontología de ciberseguridad utilizando OWL/RDF y Protégé. El objetivo es representar conceptos clave relacionados con amenazas, controles, activos y vulnerabilidades para apoyar el análisis de riesgos dentro de un entorno de ciberseguridad.

La ontología permite modelar relaciones entre amenazas y controles de seguridad, así como realizar consultas mediante SPARQL y utilizar un agente inteligente en Python para recomendar controles de mitigación.

---

# Namespace

```text
http://www.miOntologia.org/ciberseguridad#
```

---

# Clases principales

- Amenaza
- Vulnerabilidad
- Activo
- Control
- Política

---

# Relaciones principales

- afecta
- mitiga
- requiere
- protegidoPor

---

# Ejemplos de individuos

- Phishing_Corporativo
- Malware_Troyano
- FirewallCisco
- Antivirus_Kaspersky
- Servidor_Web

---

# Ejemplo de consulta SPARQL

## Consultar controles que mitigan phishing

```sparql
PREFIX ns: <http://www.miOntologia.org/ciberseguridad#>

SELECT ?control
WHERE {
    ?control ns:mitiga ns:Phishing_Corporativo .
}
```

---

# Agente Inteligente

El proyecto incluye un agente desarrollado en Python utilizando rdflib y SPARQL. El agente permite:

- Detectar amenazas
- Consultar la ontología
- Recomendar controles de seguridad
- Evaluar riesgos

Métodos principales:

- recomendar(amenaza)
- evaluar_riesgo(amenaza)

---

# Tecnologías utilizadas

- Protégé 5.6.9
- OWL/RDF
- Python
- rdflib
- SPARQL
- GitHub

---

# Autor

Alexis Fernando García Ibarra
