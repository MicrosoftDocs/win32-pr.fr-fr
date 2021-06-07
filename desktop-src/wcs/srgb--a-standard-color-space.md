---
title: Espace de couleurs standard sRVB
description: À la suite de considérations relatives à la bande passante Internet, Hewlett-Packard et Microsoft ont proposé l’adoption d’un espace de couleurs prédéfini standard, connu sous le nom d’sRGB (IEC 61966-2-1), afin de permettre un mappage précis des couleurs avec très peu de surcharge de données.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), espace de couleurs sRVB
- WCS (système de couleurs Windows), espace de couleurs sRVB
- gestion des couleurs de l’image, espace de couleurs sRVB
- gestion des couleurs, espace colorimétrique sRVB
- couleurs, espace colorimétrique sRVB
- espace colorimétrique sRVB
- espaces de couleurs, sRVB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443640"
---
# <a name="srgb-a-standard-color-space"></a>sRGB : espace de couleurs standard

À la suite de considérations relatives à la bande passante Internet, Hewlett-Packard et Microsoft ont proposé l’adoption d’un [espace de couleurs](c.md) prédéfini standard, connu sous le nom d' *sRGB* (IEC 61966-2-1), afin de permettre un mappage précis des [couleurs](c.md) avec très peu de surcharge de données.

Une version de fichier d’aide d’un livre blanc traitant des détails techniques de sRVB, sRVB. hlp, est disponible dans le \\ dossier d’aide du Guide de référence du programmeur WCS 1,0.

Différents formats de fichiers peuvent utiliser ou ajouter un indicateur pour spécifier que l’image se trouve dans l’espace de couleurs sRVB. Dans le format DIB (Device-Independent Bitmap) Windows, la définition du membre **bV5CSType** de la structure [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) sur **LCS \_ sRVB** spécifie que les couleurs DIB se trouvent dans l’espace de couleurs sRVB.

WCS 1,0 fournit la prise en charge native de sRVB. Il existe deux façons d’utiliser WCS 1,0 pour le rendu d’une image définie dans l’espace de couleurs sRVB :

**Pour afficher une image dans le contexte de périphérique**

1.  Créez un contexte de périphérique (DC) sur le périphérique d’affichage.
2.  Définissez la gestion des couleurs à l’aide de la fonction [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .
3.  Utilisez la fonction [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) pour transférer le DIB dans le DC. Tant que le membre **bV5CSMType** de la structure [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) DIB est défini sur **LCS \_ sRVB**, le système effectue la gestion des couleurs appropriée.

**Pour afficher une image en dehors du contexte de périphérique**

1.  Créez une transformation à l’aide de [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw). Le membre **lcsCSType** de la structure [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) vers laquelle pointe le paramètre *PLogColorSpace* doit être défini sur **LCS \_ sRVB**. Le paramètre *hDestProfile* indique l’espace colorimétrique du périphérique d’affichage.
2.  Utilisez la transformation de couleur créée pour mettre en correspondance l’image avant de l’afficher sur l’appareil.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Paramètres par défaut WCS 1,0 pour l’espace colorimétrique d’entrée et le profil de sortie

Si aucun espace colorimétrique d’entrée n’est spécifié, par défaut, WCS 1,0 utilise l’espace de couleurs sRVB comme espace colorimétrique d’entrée pour le [mappage des couleurs](c.md).

Quand aucun profil de sortie n’est spécifié, mais qu’un appareil par défaut est spécifié, WCS 1,0 sélectionne un profil de sortie par défaut. Si le périphérique par défaut n’est associé à aucun profil, WCS 1,0 utilise l’espace de couleurs sRVB comme profil de sortie.

Le tableau suivant présente les transformations de couleur résultantes lorsqu’un appareil par défaut n’est pas disponible.



|  &nbsp;                               | Profil de sortie spécifié                              | Profil de sortie non spécifié                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Espace colorimétrique d’entrée spécifié     | La transformation utilise les profils spécifiés.                | La transformation convertit l’espace de couleurs d’entrée connu en sRVB. |
| Espace colorimétrique d’entrée non spécifié | Transformation convertit de l’sRGB en profil de sortie connu. | La transformation de sRVB en sRVB est supposée ; aucune action n’est effectuée. |



 

## <a name="srgb-and-embedded-profiles"></a>Profils sRVB et incorporés

À partir de la version ICM 2,0, les applications qui utilisent WCS peuvent incorporer des profils dans les images. Les profils incorporés assistent les applications des utilisateurs dans le maintien d’une apparence de couleur homogène même si les images sont transmises sur Internet.

Les images qui utilisent l’espace de couleurs sRVB n’ont pas besoin d’un profil de couleurs incorporé. Étant donné qu’ils n’ont pas de profil incorporé, les images sRVB sont plus petites et plus faciles à transférer entre les canaux de données avec une bande passante limitée.

Les applications doivent définir l’indicateur de groupe de réinitialisation **LCS \_** dans l’en-tête bitmap de l’image pour indiquer que l’image utilise l’espace de couleurs sRVB. Pour plus d’informations, consultez [structures d’en-tête de bitmap Windows](using-structures-in-wcs-1-0.md) et [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 