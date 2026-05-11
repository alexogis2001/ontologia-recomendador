# Consultas SPARQL

## Obtener todos los controles

```sparql
PREFIX ns: <http://www.miOntologia.org/ciberseguridad#>

SELECT ?control
WHERE {
    ?control a ns:Control .
}
```

---

## Obtener amenazas

```sparql
PREFIX ns: <http://www.miOntologia.org/ciberseguridad#>

SELECT ?amenaza
WHERE {
    ?amenaza a ns:Amenaza .
}
```

---

## Consultar controles que mitigan phishing

```sparql
PREFIX ns: <http://www.miOntologia.org/ciberseguridad#>

SELECT ?control
WHERE {
    ?control ns:mitiga ns:Phishing_Corporativo .
}
```

---

## Consultar activos afectados

```sparql
PREFIX ns: <http://www.miOntologia.org/ciberseguridad#>

SELECT ?activo
WHERE {
    ns:Phishing_Corporativo ns:afecta ?activo .
}
```
