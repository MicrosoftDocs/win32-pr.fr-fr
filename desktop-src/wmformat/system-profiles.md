---
title: Profils système
description: Profils système
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Media Format SDK, profils système
- ASF (Advanced Systems Format), profils système
- ASF (format des systèmes avancés), profils système
- Windows Media Format SDK, ID de profil
- ASF (Advanced Systems Format), ID de profil
- ASF (format des systèmes avancés), ID de profil
- profils système, liste des
- ID de profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6389f82e93a0b27c079bd75ded9eb7d35d78a380ab72d244c5443c07f4c9ed5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807739"
---
# <a name="system-profiles"></a>Profils système

Le tableau suivant contient la liste complète des profils système pris en charge. Chaque profil listé a un nom et un ID de profil. L’ID de profil est une constante définie sur la valeur GUID affectée au profil système. Pour utiliser les ID de profil système dans votre code, vous devez inclure wmsysprf. h dans votre application. Pour obtenir des exemples montrant comment charger un profil système, consultez [pour charger un profil système](to-load-a-system-profile.md).

> [!IMPORTANT]
> les profils listés ci-dessous utilisent tous la version 8 Windows Media Audio et les codecs de Windows Media Video. il n’existe pas de profils système prédéfinis qui utilisent les codecs de la série Media 9 Windows. vous pouvez créer votre propre profil Windows Media 9 Series en utilisant un profil version 8 comme point de départ. Pour plus d’informations, consultez [réutilisation des configurations de flux](reusing-stream-configurations.md).

 



| Nom de profil                                                                      | ID de profil                     | Description                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 8 pour les Pocket PC de couleur (225 Kbits/s)                             | WMProfile \_ V80 \_ 255VideoPDA    | Utilisez ce profil lors de la création de fichiers vidéo pour la lecture sur des Pocket PC de couleur plus rapide.                                                                                 |
| Windows Media Video 8 pour les Pocket PC de couleur (150 Kbits/s)                             | WMProfile \_ V80 \_ 150VideoPDA    | Utilisez ce profil lors de la création de fichiers vidéo pour la lecture sur la plupart des Pocket PC.                                                                                         |
| Windows Media Video 8 pour les modems à accès à distance ou RNIS à canal unique (28,8 à 56 kbit/s) | WMProfile \_ V80 \_ 28856VideoMBR  | Utilisez ce profil à vitesse de transmission multiple pour les audiences cibles avec des modems d’accès à distance ou des connexions RNIS à canal unique (la bande passante est comprise entre 28,8 kbit/s et 56 kbit/s).        |
| Windows Media Video 8 pour LAN, modem câble ou xDSL (100 à 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Utilisez ce profil à vitesse de transmission multiple pour les audiences cibles avec des connexions RNIS, LAN, modem câble ou xDSL à double canal (la bande passante est comprise entre 100 Kbit/s et 500 kbit/s). |
| Windows Media Video 8 pour les modems d’accès à distance ou le réseau local (28,8 à 100 Kbits/s)                | WMProfile \_ V80 \_ 288100VideoMBR | Utilisez ce profil à vitesse de transmission multiple pour les audiences cibles avec un modem d’accès à distance, un réseau local ou des connexions RNIS à deux canaux (la bande passante est comprise entre 28,8 et 100 Kbits/s).         |
| Windows Media Video 8 pour les modems d’accès à distance (28,8 Kbits/s)                              | WMProfile \_ V80 \_ 288Video       | Utilisez ce profil pour une livraison audio/vidéo à vitesse de transmission faible sur des connexions d’accès à distance de 28,8 Kbits/s.                                                                          |
| Windows Media Video 8 pour les modems d’accès à distance (56 Kbits/s)                                | WMProfile \_ V80 \_ 56Video        | Utilisez ce profil pour une livraison audio/vidéo à vitesse de transmission faible sur des connexions d’accès à distance de 56 Kbits/s.                                                                            |
| Windows Media Video 8 pour réseau local (100 Kbits/s)                           | WMProfile \_ V80 \_ 100Video       | Utilisez ce profil pour la remise d’une vitesse de transmission moyenne sur des connexions à deux canaux RNIS, LAN ou modem câble.                                                              |
| Windows Media Video 8 pour réseau local (256 kbits/s)                           | WMProfile \_ V80 \_ 256Video       | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                     |
| Windows Media Video 8 pour réseau local (384 Kbits/s)                           | WMProfile \_ V80 \_ 384Video       | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                     |
| Windows Media Video 8 pour réseau local (768 Kbits/s)                           | WMProfile \_ V80 \_ 768Video       | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                     |
| Windows Media Video 8 pour large bande (NTSC, 700 Kbits/s)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                         |
| Windows Media Video 8 pour large bande (NTSC, 1400 Kbits/s)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                     |
| Windows Media Video 8 pour large bande (PAL, 384 Kbits/s)                               | WMProfile \_ V80 \_ 384PALVideo    | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                     |
| Windows Media Video 8 pour large bande (PAL, 700 Kbits/s)                               | WMProfile \_ V80 \_ 700PALVideo    | Utilisez ce profil pour un contenu audio/vidéo de haute qualité destiné à la lecture locale ou au téléchargement et à la lecture.                                                     |
| Windows Media audio 8 pour modem d’accès à distance (mono, 28,8 Kbits/s)                         | WMProfile \_ V80 \_ 288MonoAudio   | Utilisez ce profil pour le contenu radio et musique (audio uniquement).                                                                                                          |
| Windows Media audio 8 pour modem d’accès à distance (FM radio stéréo, 28,8 Kbits/s)              | WMProfile \_ V80 \_ 288StereoAudio | Utilisez ce profil pour le contenu radio et musique (audio uniquement).                                                                                                          |
| Windows Media audio 8 pour modem d’accès à distance (32 Kbits/s)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Utilisez ce profil pour le contenu radio et musique (audio uniquement).                                                                                                          |
| Windows Media audio 8 pour modem d’accès à distance (proche de la qualité du CD, 48 Kbits/s)                | WMProfile \_ V80 \_ 48StereoAudio  | À utiliser pour le contenu audio de la radio, de la musique et de l’usage général.                                                                                                            |
| Windows Media audio 8 pour modem d’accès à distance (qualité du CD, 64 Kbits/s)                     | WMProfile \_ V80 \_ 64StereoAudio  | Utilisez ce profil pour les audiences cibles avec des connexions Internet ou LAN à haut débit.                                                                                  |
| Windows Media audio 8 pour RNIS (meilleure que la qualité du CD, 96 Kbits/s)                  | WMProfile \_ V80 \_ 96StereoAudio  | Utilisez ce profil pour les audiences cibles avec des connexions Internet ou LAN à haut débit.                                                                                  |
| Windows Media audio 8 pour RNIS (meilleure que la qualité du CD, 128 Kbits/s)                 | WMProfile \_ V80 \_ 128StereoAudio | Utilisez ce profil pour les audiences cibles avec des connexions Internet ou LAN à haut débit.                                                                                  |
| Windows Media Video 8 pour modem d’accès à distance (pas de son, 28,8 Kbits/s)                     | WMProfile \_ V80 \_ 288VideoOnly   | Utilisez ce profil lors de la création de contenu vidéo uniquement pour les audiences cibles avec des modems d’accès à distance.                                                                         |
| Windows Media Video 8 pour modem d’accès à distance (pas de son, 56 Kbits/s)                       | WMProfile \_ V80 \_ 56VideoOnly    | Utilisez ce profil lors de la création de contenu vidéo uniquement pour les audiences cibles avec des modems d’accès à distance.                                                                         |
| Windows VBR Media 8 based Quality pour large bande                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Profil de qualité équitable à haute qualité pour le contenu VBR dont la qualité est restreinte.                                                                                     |
| Windows VBR Media 8 haute qualité pour le haut débit.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Profil le plus élevé à la meilleure qualité pour le contenu VBR dont la qualité est restreinte.                                                                                     |
| Windows Media 8 Best based VBR pour la bande passante.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Meilleur profil basé sur la qualité pour le contenu VBR dont la qualité est restreinte.                                                                                             |



 

Les profils système sont disponibles localisés pour des langues autres que l’anglais. Pour plus d’informations, consultez [profils système localisés](localized-system-profiles.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**Interface IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




