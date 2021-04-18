---
title: Fonctions WCS pour les modules de gestion des couleurs (CMM) à implémenter
description: Les fonctions suivantes doivent être implémentées par les modules de gestion des couleurs (CMMs) et exportées pour le système d’exploitation à appeler.
ms.assetid: e05129ec-9128-44f0-82c7-f4e01536d7a8
keywords:
- Windows Color System (WCS), fonctions
- WCS (système de couleurs Windows), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Système de couleurs Windows (WCS), module de gestion des couleurs (CMM)
- WCS (système de couleurs Windows), module de gestion des couleurs (CMM)
- gestion des couleurs des images, module de gestion des couleurs (CMM)
- gestion des couleurs, module de gestion des couleurs (CMM)
- couleurs, module de gestion des couleurs (CMM)
- Référence WCS, module de gestion des couleurs (CMM)
- référence pour WCS, module de gestion des couleurs (CMM)
- Module de gestion des couleurs (CMM)
- CMM (module de gestion des couleurs)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e9092c49077b1b4dda9e06829329194ec2e261
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520245"
---
# <a name="wcs-functions-for-color-management-modules-cmms-to-implement"></a>Fonctions WCS pour les modules de gestion des couleurs (CMM) à implémenter

Les fonctions suivantes doivent être implémentées par les modules de gestion des couleurs (CMMs) et exportées pour le système d’exploitation à appeler.



| Fonction                                                                     | Description                                                                               |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Détermine si les couleurs spécifiées se trouvent dans la [gamme](./g.md) de sortie d’une transformation spécifiée. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Détermine si les triplets RGB spécifiés se trouvent dans la [gamme](./g.md) de sortie d’une transformation spécifiée. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                           | Vérifie les couleurs de bitmap par rapport à une gamme de sortie.                                             |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Convertit les noms de couleurs dans un espace de couleurs nommé en nombres indexés dans un profil de couleurs |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crée un [profil de lien de périphérique](./d.md) dans le format spécifié par le consortium de couleurs international dans sa spécification de format de profil ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Accepte un tableau de profils ou un [profil de lien d’appareil](./d.md) unique et crée une transformation de couleur. Cette transformation est un mappage de l’espace colorimétrique spécifié par le premier profil à celui du deuxième profil, et ainsi de suite jusqu’au dernier. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crée un profil de couleurs d’affichage à partir d’une structure [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crée un profil de couleurs d’affichage à partir d’une structure [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Action déconseillée. Il n’existe aucune API de remplacement, car celle-ci n’a plus été utilisée. Les développeurs d’autres modules CMM n’ont pas besoin de l’implémenter. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crée une transformation de couleur qui mappe un [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) d’entrée à un espace cible facultatif, puis à un périphérique de sortie, à l’aide d’un jeu d’indicateurs qui définissent la façon dont la transformation doit être créée. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crée une transformation de couleur qui mappe un [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) d’entrée à un espace cible facultatif, puis à un périphérique de sortie, à l’aide d’un jeu d’indicateurs qui définissent la façon dont la transformation doit être créée. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Action déconseillée. Il n’existe aucune API de remplacement, car celle-ci n’a plus été utilisée. Les développeurs d’autres modules CMM n’ont pas besoin de l’implémenter. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Supprime une transformation de couleur spécifiée et libère toute mémoire qui lui est associée. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Récupère diverses informations sur le module de gestion des couleurs (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Récupère des informations sur le profil de couleurs nommé spécifié. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/) | Obtient un dictionnaire de rendu de couleur PostScript.                                             |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Récupère l' [intention de rendu](rendering-intents.md) de couleur PostScript de niveau 2 d’un profil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                   | Obtient un tableau d’espaces de couleurs PostScript.                                                      |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Indique si le profil donné est un profil ICC valide qui peut être utilisé pour la gestion des couleurs. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Convertit un tableau de couleurs d’un [espace de couleurs](rendering-intents.md) source en un espace de couleurs de destination à l’aide d’une transformation de couleur. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Traduit un RGBQuad fourni par l’application dans l’espace de [couleurs](color-spaces.md)du périphérique. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Convertit une bitmap d’un [espace de couleurs](color-spaces.md) à un autre à l’aide d’une transformation de couleur. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Convertit une bitmap d’un format défini dans un format défini différent et appelle une fonction de rappel régulièrement, si elle est spécifiée, pour signaler la progression et permettre à l’application appelante de mettre fin à la traduction. |



 

 

 