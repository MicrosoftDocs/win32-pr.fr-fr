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
ms.openlocfilehash: dbe3ca0abbe0e5b92645f6adaa1f6ebfdc44d52064d6fb8e1389420d19651b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707709"
---
# <a name="localized-system-profiles"></a>Profils système localisés

le tableau suivant répertorie les fichiers de profil système localisés fournis avec le kit de développement logiciel (SDK) Windows Media Format et les langues associées à chacune d’entre elles. Ces fichiers sont installés dans le \[ \] \\ dossier SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles Pour accéder à un fichier particulier avec les méthodes **IWMProfileManagerLanguage** , vous devez le déplacer dans le répertoire racine système avec les fichiers de profil système par défaut.



| Langage              | Nom de fichier    |
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

 

 




