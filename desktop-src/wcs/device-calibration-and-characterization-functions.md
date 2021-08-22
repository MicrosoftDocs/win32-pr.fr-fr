---
title: Fonctions d’étalonnage et de caractérisation des appareils
description: Les fonctions suivantes sont utiles pour écrire les outils d’étalonnage et de caractérisation des appareils nécessaires à l’installation et à l’étalonnage des appareils d’affichage de couleur tels que les moniteurs et les imprimantes.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Système de couleurs (WCS), fonctions
- WCS (Windows Color System), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Windows Système de couleurs (WCS), étalonnage de l’appareil
- WCS (Windows Color System), étalonnage de l’appareil
- gestion des couleurs des images, étalonnage des appareils
- gestion des couleurs, étalonnage des appareils
- couleurs, étalonnage de l’appareil
- Référence WCS, étalonnage de l’appareil
- référence pour WCS, étalonnage de l’appareil
- Windows Système de couleurs (WCS), caractérisation
- WCS (Windows Color System), caractérisation
- gestion des couleurs des images, caractérisation
- gestion des couleurs, caractérisation
- couleurs, caractérisation
- Référence WCS, caractérisation
- référence pour WCS, caractérisation
- étalonnage de l’appareil
- Auto
- caractérisation
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aea24f0a1e033df62c70674c44c9b5e9c6c0e0de1011b9ea95b9e5389d6004c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452024"
---
# <a name="device-calibration-and-characterization-functions"></a>Fonctions d’étalonnage et de caractérisation des appareils

Les fonctions suivantes sont utiles pour écrire les outils d’étalonnage et de caractérisation des appareils nécessaires à l’installation et à l’étalonnage des appareils d’affichage de couleur tels que les moniteurs et les imprimantes.



| Fonction | Description |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Ferme un handle de profil ouvert. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Crée un *profil de lien d’appareil* ICC (International Color Consortium) à partir d’un ensemble de profils de couleurs, à l’aide des intentions spécifiées. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copie les données d’un élément de profil balisé spécifié d’un profil de couleurs spécifié dans une mémoire tampon. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Récupère le nom de balise spécifié par *dwIndex* dans la table des balises d’un profil de couleurs ICC (International Color Consortium) donné, où *dwIndex* est un index de base 1 dans cette table. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Récupère le contenu du profil de couleurs en fonction d’un handle d’un profil de couleurs ouvert.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Récupère ou dérive une structure d’en-tête ICC à partir du profil de couleurs ICC ou du profil XML WCS. Les pilotes et les applications doivent supposer que retourne la **valeur true** indique qu’un en-tête correctement structuré est retourné. Chaque balise doit toujours être validée indépendamment à l’aide de l’API ICM2 héritée ou des API de schéma XML. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Récupère le nombre d’éléments avec balises dans un profil de couleurs donné. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | récupère le dictionnaire de rendu de couleur de PostScript niveau 2 à partir du profil de couleurs ICC spécifié. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | récupère l' [intention de rendu](r.md) de couleur de niveau 2 PostScript à partir d’un profil de couleurs ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | récupère le PostScript tableau d' [espace de couleurs](c.md) de niveau 2 à partir d’un profil de couleurs ICC. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Signale si une balise ICC (International Color Consortium) spécifiée est présente dans le profil de couleurs spécifié. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | permet de déterminer si le profil spécifié est un profil ICC (International color Consortium) valide ou un handle de profil WCS (Windows Color System) valide qui peut être utilisé pour la gestion des couleurs. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crée un handle vers un profil de couleurs spécifié. Le descripteur peut ensuite être utilisé dans d’autres fonctions de gestion des profils. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Définit les données d’élément pour un élément de profil balisé dans un profil de couleurs ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crée dans un profil de couleurs ICC spécifié une nouvelle balise qui référence les mêmes données qu’une balise existante. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Définit la taille d’un élément balisé dans un profil de couleurs ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Définit les données d’en-tête dans un profil de couleurs ICC spécifié. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Détermine si la gestion du système de l’état d’étalonnage de l’affichage est activée. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Détermine si la gestion du système de l’état d’étalonnage de l’affichage est activée. |



 

 

 




