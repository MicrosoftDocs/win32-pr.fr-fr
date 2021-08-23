---
title: Fonctions (API d’agrandissement)
description: Cette section contient des informations de référence sur les fonctions d’API d’agrandissement.
ms.assetid: 82b7d82b-b8cd-4f80-ad30-f7db20c57742
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 4513258f5c4bbb1cafe9ef22b35a4708c63e1c45be353b55c8bda1e20c4fce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644619"
---
# <a name="magnification-api-functions"></a>Fonctions de l’API zoom

Cette section contient des informations de référence sur les fonctions d’API d’agrandissement.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|:---|:---|
| [**MagGetColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetcoloreffect)<br/> | Obtient la matrice de transformation de couleur pour un contrôle magnifier.<br/> |
| [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect)<br/>  |  Récupère la matrice de transformation de couleur associée à la loupe plein écran.<br/> |
| [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform)<br/>  | Récupère les paramètres d’agrandissement pour la loupe plein écran.<br/>  |
| [***MagGetImageScalingCallback** _ _](/windows/win32/api/Magnification/nf-magnification-maggetimagescalingcallback)<br/>  | _ * déconseillé dans Windows 7 et versions ultérieures * *<br/>Récupère la fonction de rappel inscrit qui implémente une transformation personnalisée pour la mise à l’échelle de l’image. <br/> |
| [**MagGetInputTransform**](/windows/win32/api/Magnification/nf-magnification-maggetinputtransform)<br/>  | Récupère la transformation d’entrée actuelle pour le stylet et l’entrée tactile, représentée sous la forme d’un rectangle source et d’un rectangle de destination.<br/>  |
| [**MagGetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-maggetwindowfilterlist)<br/>  | Récupère la liste des fenêtres qui sont agrandies ou exclues de l’agrandissement.<br/>  |
| [**MagGetWindowSource**](/windows/win32/api/Magnification/nf-magnification-maggetwindowsource)<br/>  | Obtient le rectangle de la zone qui est agrandie.<br/>  |
| [**MagGetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-maggetwindowtransform)<br/>  | Récupère la matrice de transformation associée à un contrôle magnifier. <br/>  |
| [***MagImageScalingCallback** _ _](/windows/win32/api/Magnification/nc-magnification-magimagescalingcallback)<br/>  | _ * déconseillé dans Windows 7 et versions ultérieures * *<br/>Prototype pour une fonction de rappel qui implémente une transformation personnalisée pour la mise à l’échelle de l’image.<br/>  |
| [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize)<br/>  | Crée et initialise les objets d’exécution de la loupe. <br/>  |
| [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)<br/>  | >définit la matrice de transformation des couleurs pour un contrôle magnifier.<br/>  |
| [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect)<br/>  | Modifie la matrice de transformation de couleur associée à la loupe plein écran.<br/>  |
| [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)<br/>  | Modifie les paramètres d’agrandissement de la loupe plein écran.<br/>  |
| [***MagSetImageScalingCallback** _ _](/windows/win32/api/Magnification/nf-magnification-magsetimagescalingcallback)<br/>  | _ * déconseillé dans Windows 7 et versions ultérieures * *<br/>Définit la fonction de rappel pour le filtrage et la mise à l’échelle des images externes.<br/>  |
| [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)<br/>  | Définit la transformation d’entrée active actuelle pour le stylet et l’entrée tactile, représentée sous la forme d’un rectangle source et d’un rectangle de destination.<br/>  |
| [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist)<br/>  | Définit la liste des fenêtres à agrandir ou la liste des fenêtres à exclure de l’agrandissement.<br/>  |
| [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource)<br/>  | Définit le rectangle source pour la fenêtre d’agrandissement.<br/>  |
| [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform)<br/>  | Définit la matrice de transformation pour un contrôle magnifier. <br/>  |
| [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)<br/>  | Affiche ou masque le curseur système.<br/>  |
| [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize)<br/>  | Détruit les objets d’exécution de la loupe.<br/>  |

## <a name="related-topics"></a>Rubriques connexes

[Informations de référence](entry-magapi-ref.md)
