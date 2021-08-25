---
title: Fonctions avancées pour une utilisation en dehors d’un contexte d’appareil
description: Ces fonctions fournissent des fonctionnalités de gestion de couleurs avancées en dehors des contextes de périphérique.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Système de couleurs (WCS), fonctions
- WCS (Windows Color System), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685b9fe1c7139be1c54e1b158a03c1de54d01b2b80ec4cab4b86603680c6d957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814612"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Fonctions avancées pour une utilisation en dehors d’un contexte d’appareil

Ces fonctions fournissent des fonctionnalités de gestion de couleurs avancées en dehors des contextes de périphérique.



| Fonction                                                           | Description                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (ou **ApplyCallbackFunction**) est une fonction de rappel que vous implémentez pour mettre à jour les données de configuration WCS pendant que la boîte de dialogue affichée par la fonction [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) s’exécute. |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Vérifie si les pixels d’une bitmap spécifiée se trouvent dans la [gamme](g.md) de sortie d’une transformation spécifiée. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Détermine si les couleurs d’un tableau se trouvent dans la [gamme](g.md) de sortie d’une transformation spécifiée. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Convertit les noms de couleurs dans un espace de couleurs nommé en nombres d’index dans un profil de couleurs ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Accepte un tableau de profils ou un [profil de lien d’appareil](d.md) unique et crée une transformation de couleur que les applications peuvent utiliser pour effectuer le mappage des couleurs. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Supprime une transformation de couleur donnée. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Récupère diverses informations sur le module de gestion des couleurs (CMM) qui a créé la transformation de couleur spécifiée. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Récupère des informations sur le profil de couleurs nommé ICC (International Color Consortium) qui est spécifié dans le premier paramètre. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Fonction de rappel fournie par l’application pour signaler la progression. Le nom de cette fonction est également défini par l’application.                                                 |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Vous permet de sélectionner le module de gestion des couleurs par défaut (CMM) à utiliser. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Fournit un contrôle utilisateur sur la gestion des couleurs par le biais d’une boîte de dialogue.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Convertit les couleurs de la bitmap à l’aide d’une transformation de couleur.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Convertit un tableau de couleurs de l' [espace de couleurs](c.md) source en espace de couleurs de destination, tel que défini par une transformation de couleur. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Détermine si les couleurs d’un tableau se trouvent dans la gamme de sortie d’une transformation de couleur WCS spécifiée.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Convertit un tableau de couleurs de l’espace de couleurs source en espace de couleurs de destination, tel que défini par une transformation de couleur.                                                |



 

 

 




