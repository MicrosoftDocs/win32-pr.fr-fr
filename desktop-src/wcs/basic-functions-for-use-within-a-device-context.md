---
title: Fonctions de base à utiliser dans un contexte d’appareil
description: Les fonctions WCS suivantes offrent des fonctionnalités de mappage de couleurs de base dans les contextes de périphérique. Elles sont utiles pour toutes les applications qui doivent implémenter la gestion des couleurs avec une faible surcharge et une intervention minimale de l’utilisateur.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Système de couleurs (WCS), fonctions
- WCS (Windows Color System), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Windows Système de couleurs (WCS), contextes de périphérique
- WCS (Windows Color System), contextes de périphérique
- gestion des couleurs des images, contextes de périphérique
- gestion des couleurs, contextes de périphérique
- couleurs, contextes de périphérique
- Référence WCS, contextes de périphérique
- référence pour WCS, contextes de périphérique
- contextes de périphérique
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a934c1737a7eea8b32a9589325e73300db82334a40ee47b411922b89cb61f568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118210978"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Fonctions de base à utiliser dans un contexte d’appareil

Les fonctions WCS suivantes offrent des fonctionnalités de [mappage de couleurs](c.md) de base dans les contextes de périphérique. Elles sont utiles pour toutes les applications qui doivent implémenter la gestion des couleurs avec une faible surcharge et une intervention minimale de l’utilisateur.



| Fonction                                                           | Description                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Vérifie si les couleurs spécifiées se trouvent dans la gamme d’appareils.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Corrige les entrées dans une palette pour un contexte de périphérique.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Effectue un mappage des couleurs à des fins de préversion.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Crée un espace de couleurs.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Supprime un espace de couleurs.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Énumère les profils de couleur de sortie disponibles pour un contexte de périphérique donné.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Fonction de rappel définie par l’application pour [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). Le nom de cette fonction est également défini par l’application. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtient l’espace colorimétrique d’entrée actuel dans un contexte de périphérique. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Obtient le profil de couleur de sortie actuel d’un contexte de périphérique.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Obtient la structure [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) d’un contexte de périphérique.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Définit l’espace colorimétrique d’entrée d’un contexte de périphérique.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Active ou désactive la gestion des couleurs dans un contexte de périphérique.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Définit le profil de couleur de sortie pour un contexte de périphérique donné.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Énumère tous les profils de couleurs qui répondent aux critères d’énumération dans la portée de gestion des profils spécifiée.                                      |



 

 

 




