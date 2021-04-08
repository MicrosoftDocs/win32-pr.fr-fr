---
title: Modèles de conformité des périphériques vidéo
description: Modèles de conformité des périphériques vidéo
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows Media Format SDK, modèles de conformité des appareils
- ASF (Advanced Systems Format), modèles de conformité des appareils
- ASF (format des systèmes avancés), modèles de conformité des appareils
- Windows Media Format SDK, modèles de conformité des périphériques vidéo
- ASF (Advanced Systems Format), modèles de conformité des périphériques vidéo
- ASF (format des systèmes avancés), modèles de conformité des périphériques vidéo
- Codec Windows Media Video 9, modèles de conformité des périphériques vidéo
- codecs, codec Windows Media Video 9
- modèles de conformité des appareils, vidéo
- modèles de conformité des périphériques vidéo
- modèles, modèles de conformité des périphériques vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6735d029bc2339296fa2a0af8a48ace3303ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840805"
---
# <a name="video-device-conformance-templates"></a>Modèles de conformité des périphériques vidéo

Les tableaux suivants répertorient les modèles de conformité des appareils et les paramètres associés pour le codec Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Profil simple, niveau bas



| Paramètre                                | Valeur                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Chaîne de modèle                          | "SP@LL"                                                                               |
| Appareils appropriés                      | Combinés sans fil (solution Microsoft Windows-Powered SmartPhone et appareils similaires) |
| Résolution maximale                       | 176 x 144                                                                             |
| Fréquence d’images maximale                       | 15 fps                                                                                |
| Vitesse de transmission maximale                         | 96 Kbits/s                                                                               |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 20 (environ 3,4 secondes avec une vitesse de transmission maximale)                                            |
| Encodage entrelacé                      | Non                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Profil simple, niveau moyen



| Paramètre                                | Valeur                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Chaîne de modèle                          | "SP@ML"                                                                              |
| Appareils appropriés                      | Ordinateurs portables et assistantsHigh de données personnelles combinés sans fil<br/> |
| Résolution maximale                       | 352 x 288                                                                            |
| Fréquence d’images maximale                       | 15 ips @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Vitesse de transmission maximale                         | 384 Kbits/s                                                                             |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 77 (environ 3,3 secondes avec une vitesse de transmission maximale)                                           |
| Encodage entrelacé                      | Non                                                                                   |



 

## <a name="generic-simple-profile"></a>Profil simple générique

Un flux conforme aux limitations algorithmiques du profil simple, mais qui ne tient pas dans l’une des spécifications de niveau, se voit attribuer « SP » comme chaîne de modèle de conformité de périphérique.

## <a name="main-profile-low-level"></a>Profil principal, niveau bas



| Paramètre                                | Valeur                                       |
|------------------------------------------|---------------------------------------------|
| Chaîne de modèle                          | "MP@LL"                                     |
| Appareils appropriés                      | Zones déroulantes                               |
| Résolution maximale                       | 352 x 288                                   |
| Fréquence d’images maximale                       | 30 i/s                                      |
| Vitesse de transmission maximale                         | 2 Mbits/s                                      |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 306 (environ 2,5 secondes avec une vitesse de transmission maximale) |
| Encodage entrelacé                      | Non                                          |



 

## <a name="main-profile-medium-level"></a>Profil principal, niveau moyen



| Paramètre                                | Valeur                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Chaîne de modèle                          | "MP@ML"                                                                                                                |
| Appareils appropriés                      | Définir les ordinateurs boxesSlower les plus à l’aide de DirectX Video Acceleration<br/> Lecteurs DVD compatibles Windows Media<br/> |
| Résolution maximale                       | 720 x 576                                                                                                              |
| Fréquence d’images maximale                       | 30 i/s @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Vitesse de transmission maximale                         | 10 Mbits/s                                                                                                                |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 611 (environ 1 seconde avec une vitesse de transmission maximale)                                                                               |
| Encodage entrelacé                      | Oui                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Profil principal, niveau supérieur



| Paramètre                                | Valeur                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chaîne de modèle                          | "MP@HL"                                                                                                                                                               |
| Appareils appropriés                      | Ordinateurs utilisant DirectX Video AccelerationHigh-Definition lecteurs DVD compatibles Windows Media<br/> Cinéma numérique<br/> streaming haute définition<br/> |
| Résolution maximale                       | 1920 x 1080                                                                                                                                                           |
| Fréquence d’images maximale                       | 30 i/s @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Vitesse de transmission maximale                         | 20 Mbits/s                                                                                                                                                               |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 2442 (environ 2,66 secondes avec une vitesse de transmission maximale)                                                                                                                         |
| Encodage entrelacé                      | Oui                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Profil principal générique

Un flux conforme aux limitations algorithmiques du profil principal, mais qui ne tient pas dans l’une des spécifications de niveau, est affecté « MP » comme chaîne de modèle de conformité de périphérique.

## <a name="complex-profile"></a>Profil complexe



| Paramètre       | Valeur                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Chaîne de modèle | CP                                                                                                                                   |
| Notes         | Le profil complexe n’a pas de limitations explicites. Il est utilisé pour activer tous les algorithmes de codec, généralement à des fins de démonstration. |



 

Les tableaux suivants répertorient les paramètres des modèles de conformité des appareils pour le codec d’image Windows Media Video 9.

## <a name="video-image-level-1"></a>Image vidéo-niveau 1



| Paramètre                                | Valeur                                       |
|------------------------------------------|---------------------------------------------|
| Chaîne de modèle                          | I1                                        |
| Résolution maximale                       | 352 x 288                                   |
| Fréquence d’images maximale                       | 30 i/s                                      |
| Vitesse de transmission maximale                         | 192 Kbits/s                                    |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 39 (environ 3,26 secondes avec une vitesse de transmission maximale) |
| Encodage entrelacé                      | Non                                          |



 

## <a name="video-image-level-2"></a>Image vidéo-niveau 2



| Paramètre                                | Valeur                                       |
|------------------------------------------|---------------------------------------------|
| Chaîne de modèle                          | I2                                        |
| Résolution maximale                       | 1024 x 768                                  |
| Fréquence d’images maximale                       | 30 i/s                                      |
| Vitesse de transmission maximale                         | 384 Kbits/s                                    |
| Taille maximale de la mémoire tampon (en unités de 16384 bits) | 77 (environ 3,26 secondes avec une vitesse de transmission maximale) |
| Encodage entrelacé                      | Non                                          |



 

## <a name="generic-video-image"></a>Image vidéo générique

Un flux d’image vidéo qui ne tient pas dans l’une des spécifications de niveau se verra attribuer « I » comme chaîne de modèle de conformité de périphérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modèles de conformité des périphériques audio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Paramètres du modèle de conformité des appareils**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaisons recommandées de modèles de conformité des appareils**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





