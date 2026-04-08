# 📱 Converter — Android App


> A simple Android application to convert **temperatures** (°C ↔ °F) and **distances** (KM ↔ Miles), built with two tabs, a Quit menu, and a back-press confirmation dialog.

---

## 🎬 Vidéo Explicatif

<!-- ✅ AJOUTER LA VIDÉO ICI -->
<!-- Option 1 — YouTube : remplace le lien ci-dessous -->
<!--
[![Voir la démo](https://img.youtube.com/vi/VOTRE_VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VOTRE_VIDEO_ID)
-->

<!-- Option 2 — Vidéo locale hébergée sur GitHub -->
<!--
https://github.com/VOTRE_USERNAME/VOTRE_REPO/assets/VOTRE_ID/votre-video.mp4
-->

> 📌 *La vidéo explicative sera ajoutée ici prochainement.*

---

## ✨ Fonctionnalités

| Fonctionnalité | Description |
|---|---|
| 🌡️ Onglet **C ↔ F** | Convertir Celsius en Fahrenheit et vice versa |
| 📏 Onglet **KM ↔ Miles** | Convertir kilomètres en miles et vice versa |
| 🚪 Menu **Quitter** | Bouton dans la toolbar pour fermer l'application |
| 🔙 Touche **Retour** | Interceptée avec une boîte de dialogue de confirmation |

---

## 📐 Formules de conversion

```
°C  →  °F  :   (C × 9/5) + 32
°F  →  °C  :   (F − 32) × 5/9

KM  →  Miles :  KM × 0.621371
Miles  →  KM :  Miles × 1.60934
```

---

## 🗂️ Structure du projet

```
app/src/main/
├── java/com/example/converter/
│   ├── MainActivity.java          # Activité principale (tabs + menu + retour)
│   ├── TemperatureFragment.java   # Fragment onglet C <-> F
│   └── DistanceFragment.java      # Fragment onglet KM <-> Miles
│
└── res/
    ├── layout/
    │   ├── activity_main.xml      # Layout principal (Toolbar + TabLayout + ViewPager2)
    │   ├── fragment_temperature.xml
    │   └── fragment_distance.xml
    └── menu/
        └── main_menu.xml          # Menu "Quitter"
```

---

## ⚙️ Technologies utilisées

- **Java** — Langage principal
- **ViewPager2** — Navigation entre les onglets
- **TabLayout** (Material Design) — Affichage des onglets
- **Fragment** — Chaque onglet est un fragment indépendant
- **AlertDialog** — Boîte de dialogue de confirmation
- **OnBackPressedDispatcher** — Gestion moderne du bouton Retour

---

## 📦 Dépendances (`build.gradle`)

```groovy
dependencies {
    implementation(libs.appcompat)
    implementation(libs.material)
    implementation(libs.activity)
    implementation(libs.constraintlayout)

    // ViewPager2 pour la navigation par onglets
    implementation("androidx.viewpager2:viewpager2:1.0.0")

    testImplementation(libs.junit)
    androidTestImplementation(libs.ext.junit)
    androidTestImplementation(libs.espresso.core)
}
```

---

## 🚀 Installation & Lancement

1. **Cloner** le dépôt :
   ```bash
   git clone https://github.com/VOTRE_USERNAME/converter-android.git
   ```

2. **Ouvrir** dans Android Studio

3. **Synchroniser** Gradle (`File → Sync Project with Gradle Files`)

4. **Lancer** sur un émulateur ou un appareil physique (API 21+)

---

## 📸 Aperçu

| Onglet Température | Onglet Distance | Menu Quitter |
|---|---|---|
| *(screenshot)* | *(screenshot)* | *(screenshot)* |

> 💡 Remplacez les cellules ci-dessus avec vos propres captures d'écran.

---

## 🐛 Problèmes connus & Solutions

### `onBackPressed` déprécié
> **Erreur :** `onBackPressed is no longer called for back gestures`

**Solution :** Utiliser `OnBackPressedDispatcher` à la place :
```java
getOnBackPressedDispatcher().addCallback(this, new OnBackPressedCallback(true) {
    @Override
    public void handleOnBackPressed() {
        showQuitDialog();
    }
});
```

---

---

## 📄 Licence

Ce projet est réalisé dans le cadre d'un laboratoire académique.# 📱 Converter — Android App


> A simple Android application to convert **temperatures** (°C ↔ °F) and **distances** (KM ↔ Miles), built with two tabs, a Quit menu, and a back-press confirmation dialog.

---

## 🎬 Vidéo Explicatif

<!-- ✅ AJOUTER LA VIDÉO ICI -->
<!-- Option 1 — YouTube : remplace le lien ci-dessous -->
<!--
[![Voir la démo](https://img.youtube.com/vi/VOTRE_VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VOTRE_VIDEO_ID)
-->

<!-- Option 2 — Vidéo locale hébergée sur GitHub -->
<!--
https://github.com/VOTRE_USERNAME/VOTRE_REPO/assets/VOTRE_ID/votre-video.mp4
-->

> 📌 *La vidéo explicative sera ajoutée ici prochainement.*

---

## ✨ Fonctionnalités

| Fonctionnalité | Description |
|---|---|
| 🌡️ Onglet **C ↔ F** | Convertir Celsius en Fahrenheit et vice versa |
| 📏 Onglet **KM ↔ Miles** | Convertir kilomètres en miles et vice versa |
| 🚪 Menu **Quitter** | Bouton dans la toolbar pour fermer l'application |
| 🔙 Touche **Retour** | Interceptée avec une boîte de dialogue de confirmation |

---

## 📐 Formules de conversion

```
°C  →  °F  :   (C × 9/5) + 32
°F  →  °C  :   (F − 32) × 5/9

KM  →  Miles :  KM × 0.621371
Miles  →  KM :  Miles × 1.60934
```

---

## 🗂️ Structure du projet

```
app/src/main/
├── java/com/example/converter/
│   ├── MainActivity.java          # Activité principale (tabs + menu + retour)
│   ├── TemperatureFragment.java   # Fragment onglet C <-> F
│   └── DistanceFragment.java      # Fragment onglet KM <-> Miles
│
└── res/
    ├── layout/
    │   ├── activity_main.xml      # Layout principal (Toolbar + TabLayout + ViewPager2)
    │   ├── fragment_temperature.xml
    │   └── fragment_distance.xml
    └── menu/
        └── main_menu.xml          # Menu "Quitter"
```

---

## ⚙️ Technologies utilisées

- **Java** — Langage principal
- **ViewPager2** — Navigation entre les onglets
- **TabLayout** (Material Design) — Affichage des onglets
- **Fragment** — Chaque onglet est un fragment indépendant
- **AlertDialog** — Boîte de dialogue de confirmation
- **OnBackPressedDispatcher** — Gestion moderne du bouton Retour

---

## 📦 Dépendances (`build.gradle`)

```groovy
dependencies {
    implementation(libs.appcompat)
    implementation(libs.material)
    implementation(libs.activity)
    implementation(libs.constraintlayout)

    // ViewPager2 pour la navigation par onglets
    implementation("androidx.viewpager2:viewpager2:1.0.0")

    testImplementation(libs.junit)
    androidTestImplementation(libs.ext.junit)
    androidTestImplementation(libs.espresso.core)
}
```

---

## 🚀 Installation & Lancement

1. **Cloner** le dépôt :
   ```bash
   git clone https://github.com/VOTRE_USERNAME/converter-android.git
   ```

2. **Ouvrir** dans Android Studio

3. **Synchroniser** Gradle (`File → Sync Project with Gradle Files`)

4. **Lancer** sur un émulateur ou un appareil physique (API 21+)

---

## 📸 Aperçu

| Onglet Température | Onglet Distance | Menu Quitter |
|---|---|---|
| *(screenshot)* | *(screenshot)* | *(screenshot)* |

> 💡 Remplacez les cellules ci-dessus avec vos propres captures d'écran.

---

## 🐛 Problèmes connus & Solutions

### `onBackPressed` déprécié
> **Erreur :** `onBackPressed is no longer called for back gestures`

**Solution :** Utiliser `OnBackPressedDispatcher` à la place :
```java
getOnBackPressedDispatcher().addCallback(this, new OnBackPressedCallback(true) {
    @Override
    public void handleOnBackPressed() {
        showQuitDialog();
    }
});
```

---

---

## 📄 Licence

Ce projet est réalisé dans le cadre d'un laboratoire académique.