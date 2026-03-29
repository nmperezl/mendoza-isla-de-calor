# Isla de Calor - Mendoza AMM

Aplicación para analizar la **isla de calor urbana de Mendoza** usando **Google Earth Engine**.

## 🛰️ Datos utilizados

- **Satélite:** Landsat 8 (OLI/TIRS)  
- **Periodo de análisis:** 1 de enero 2025 → 30 de marzo 2025  
- **Área de estudio:** Mendoza, Argentina (área de influencia de 15 km alrededor del entro de la ciudad de mendoza)  
- **Selección de imagen:** La imagen menos nublada dentro del periodo  - Resolución espacial de 30m
- **Nota:** Landsat mide temperatura **de día** (~10:30 AM), no hay datos nocturnos.

---

##  Capas y análisis

1. **Temperatura superficial (LST)**
   - Muestra el calor del suelo. 
   - Rojo = zonas calientes (asfalto, ciudad)  
   - Verde = zonas frías (vegetación, agua)

2. **NDVI - Vegetación**
   - Indica actividad fotosintética y salud de la vegetación  
   - Verde oscuro = vegetación sana  
   - Amarillo = vegetación débil  
   - Blanco = urbano / suelo

3. **FVC - Cobertura vegetal**
   - Muestra el porcentaje de suelo cubierto por vegetación  
   - Verde = mucha cobertura  
   - Marrón = suelo urbano

4. **Hotspots urbanos**
   - Detecta zonas más calientes dentro de áreas urbanas usando umbral basado en media + desviación estándar  

---


## 🔗 Acceso a la app

La app interactiva se puede ver aquí:  
[Mendoza Isla de Calor](https://ee-naperez817.projects.earthengine.app/view/mendoza-isla-de-calor)
