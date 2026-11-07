# Banc d'Essai : Surveillance Prédictive et Analyse Vibratoire de Moteur Industriel

Système embarqué d'acquisition et de surveillance en temps réel de la santé d'un moteur électrique industriel (Condition Monitoring), basé sur microcontrôleur Arduino Uno. Le dispositif mesure en continu les vibrations triaxiales et la température de fonctionnement pour anticiper les défaillances mécaniques selon les principes de la Maintenance 4.0.

---

## ⚙️ Spécifications Matérielles
- **Microcontrôleur** : Arduino Uno (ATmega328P).
- **Capteur d'accélération & vibrations** : MPU6050 (Accéléromètre 3 axes + Gyroscope via bus I2C).
- **Capteur thermo-hygrométrique** : DHT22 (mesure numérique haute précision de température).
- **Interface visuelle locale (IHM)** : Écran LCD 16x2 avec module d'interface série I2C (PCF8574).
- **Indicateur d'alarme** : LED rouge de signalisation de dépassement de seuil critique.

---

## 📊 Logique Métier & Algorithme de Surveillance
1. **Acquisition multiaxiale** : Lecture des accélérations brutes ($a_x, a_y, a_z$) et calcul de la magnitude globale d'accélération.
2. **Surveillance thermique** : Détection des surchauffes moteur ($T > 45^\circ\text{C}$).
3. **Seuils d'alarme prédictifs** :
   - Vibration critique : Accélération résultante supérieure à $12\,\text{m/s}^2$.
   - Température critique : Température supérieure à $45^\circ\text{C}$.
4. **Affichage dynamique en temps réel** : Restitution instantanée de l'état mécanique (`NORMAL` ou `VIB_ALARM` / `TEMP_ALARM`) sur l'écran LCD.

---

## 🔗 Simulation Interactive en Direct (Wokwi)
Visualisez le fonctionnement du banc, ajustez les accélérations et observez l'affichage LCD en temps réel :  
👉 **[Lancer la simulation du banc moteur sur Wokwi](https://wokwi.com/projects/480033720169224193)**

---

## 👨‍💻 Auteur
**Ahmed El Ayachi**  
*Ingénieur en Informatique Industrielle et Systèmes Embarqués*
