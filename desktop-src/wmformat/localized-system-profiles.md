---
title: Profils système localisés
description: Profils système localisés
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Media Format SDK, profils système
- ASF (Advanced Systems Format), profils système
- ASF (format des systèmes avancés), profils système
- Windows Media Format SDK, profils système localisés
- ASF (Advanced Systems Format), profils système localisés
- ASF (format des systèmes avancés), profils système localisés
- profils système, localisés
- profils système localisés, liste de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaeecdf1d1d62d78df18e0ac1c5bffbf39f9778
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030760"
---
# <a name="localized-system-profiles"></a>Profils système localisés

Le tableau suivant répertorie les fichiers de profil système localisés fournis avec le kit de développement logiciel (SDK) Windows Media format et les langues associées à chacun d’eux. Ces fichiers sont installés dans le \[ \] \\ dossier SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles Pour accéder à un fichier particulier avec les méthodes **IWMProfileManagerLanguage** , vous devez le déplacer dans le répertoire racine système avec les fichiers de profil système par défaut.



| Language              | Nom de fichier    |
|-----------------------|--------------|
| Arabe                | WMPrfAra. prx |
| Chinois – simplifié  | WMPrfCHS. prx |
| Chinois – traditionnel | WMPrfCHT. prx |
| Tchèque                 | WMPrfCsy. prx |
| Danois                | WMPrfDan. prx |
| Néerlandais                 | WMPrfNld. prx |
| Finnois               | WMPrfFin. prx |
| Français                | WMPrfFra. prx |
| Allemand                | WMPrfDeu. prx |
| Grec                 | WMPrfEll. prx |
| Hébreu                | WMPrfHeb. prx |
| Hongrois             | WMPrfHun. prx |
| Italien               | WMPrfIta. prx |
| Japonais              | WMPrfJpn. prx |
| Coréen                | WMPrfKor. prx |
| Norvégien             | WMPrfNor. prx |
| Polonais                | WMPrfPlk. prx |
| Portugais – Brésil   | WMPrfPtb. prx |
| Portugais – Portugal | WMPrfPtg. prx |
| Russe               | WMPrfRus. prx |
| Slovaque                | WMPrfSky. prx |
| Slovène             | WMPrfSlv. prx |
| Espagnol               | WMPrfEsp. prx |
| Suédois               | WMPrfSve. prx |
| Turc               | WMPrfTrk. prx |



 

Vous pouvez définir la langue de l’objet gestionnaire de profils en appelant la méthode [**IWMProfileManagerLanguage :: SetUserLanguageID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) . Pour la plupart des langues, seul l’identificateur de langue primaire dans l’ID de langue est examiné. Les exceptions concernent les langues chinoises et portugaises, où l’identificateur de langue secondaire est également utilisé. Le tableau suivant montre comment créer un LANGID pour spécifier dans la méthode **SetUserLanguageID** .



| Primaire-langue secondaire | MAKELANGID macro)                                             |
|----------------------------|--------------------------------------------------------------|
| Chinois (simplifié)       | MAKELANGID (langue \_ chinoise, sous-langue \_ chinois \_ simplifié)     |
| Chinois (traditionnel)      | MAKELANGID (langue \_ chinoise, sous-langue- \_ chinois \_ Singapour)      |
| Portugais (Brésil)        | MAKELANGID ( \_ portugais du Brésil, sublang \_ portugais \_ brésilien) |
| Portugais (Portugal)      | MAKELANGID (portugais (LANG \_ ), sous-lang \_ portugais)            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> <dt>

[**Profils système**](system-profiles.md)
</dt> </dl>

 

 




