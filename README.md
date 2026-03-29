*Dos experimentos** para analizar la **isla de calor urbana en Mendoza** usando **Google Earth Engine**

# Isla de Calor - Mendoza AMM (Landsat 8 - 30m)

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




## Frescura Urbana – Mendoza (Sentinel‑2, 10 m)

Aplicación para analizar un **proxy de isla de calor urbana** en Mendoza usando **Sentinel‑2** y **Google Earth Engine**, con mayor resolución espacial que Landsat (10 m).  

🔗 **App interactiva:** [Mendoza – Frescura Urbana (Sentinel‑2)](https://ee-naperez817.projects.earthengine.app/view/mendoza---isla-de-calor-sentinel-2--10m)

---

## 🛰️ Datos utilizados

- **Satélite:** Sentinel‑2 (S2_SR_HARMONIZED)  
- **Periodo de análisis:** 1 de enero → 31 de marzo 2024  
- **Área de estudio:** Mendoza, Argentina (±15 km del centro)  
- **Selección de imagen:** La imagen menos nublada (<20 % nubes)  
- **Resolución espacial:** 10 m para bandas ópticas
- **Nota:** Sentinel‑2 no mide temperatura directa; se calculan **índices de frescura urbana** para interpretar el calor de superficie.

---

## Capas y análisis

1. **NDVI – Vegetación**  
   - Indica salud de la vegetación (mayor valor = más vegetación)  
   - Verde oscuro = vegetación sana  
   - Amarillo = vegetación débil  
   - Blanco = urbano / suelo

2. **NDWI – Humedad / Agua**  
   - Indica presencia de agua en superficie y humedad del suelo  

3. **NDBI – Superficies edificadas**  
   - Indica áreas urbanas y construidas  

4. **Índice de frescura**  
   - Combina vegetación + agua – áreas edificadas  
   - Alto valor → más fresco  
   - Bajo valor → más caliente

5. **Hotspots urbanos**  
   - Zonas urbanas con **bajo indice de frescura**, identificando los sectores más “calientes”  


