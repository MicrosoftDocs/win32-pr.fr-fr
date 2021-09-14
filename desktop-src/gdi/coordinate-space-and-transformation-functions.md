---
description: Les fonctions suivantes sont utilisées avec des espaces de coordonnées et des transformations.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Fonctions d’espace de coordonnées et de transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e561f5cc9784439f5bef4f696e98d5919cb052
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227892"
---
# <a name="coordinate-space-and-transformation-functions"></a>Fonctions d’espace de coordonnées et de transformation

Les fonctions suivantes sont utilisées avec des espaces de coordonnées et des transformations.



| Fonction                                                                       | Description                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ClientToScreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Convertit les coordonnées de la zone cliente d’un point spécifié en coordonnées d’écran.                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Concatène deux transformations de l’espace universel avec les espaces de page.                                                                      |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Convertit les coordonnées de l’appareil en coordonnées logiques.                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Récupère la position actuelle en coordonnées logiques.                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | Obtient les préférences d’orientation de l’affichage.                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Récupère le mode graphique actuel pour le contexte de périphérique spécifié.                                                            |
| [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Récupère le mode de mappage actuel.                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Récupère les étendues x et y de la fenêtre d’affichage actuelle pour le contexte de périphérique spécifié.                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Récupère les coordonnées x et y de l’origine de la fenêtre d’affichage pour le contexte de périphérique spécifié.                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Récupère les étendues x et y de la fenêtre pour le contexte de périphérique spécifié.                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Récupère les coordonnées x et y de l’origine de la fenêtre pour le contexte de périphérique spécifié.                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Récupère l’espace universel actuel pour la transformation d’espace de page.                                                                  |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Convertit les coordonnées logiques en coordonnées de périphérique.                                                                            |
| [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Convertit (mappe) un ensemble de points d’un espace de coordonnées par rapport à une fenêtre en un espace de coordonnées par rapport à une autre fenêtre. |
| [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Modifie la transformation universelle d’un contexte de périphérique à l’aide du mode spécifié.                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Modifie l’origine de la fenêtre d’affichage pour un contexte de périphérique à l’aide des décalages horizontal et vertical spécifiés.                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Modifie l’origine de la fenêtre pour un contexte de périphérique à l’aide des décalages horizontal et vertical spécifiés.                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Modifie la fenêtre d’affichage pour un contexte de périphérique à l’aide des ratios formés par le multiplicands et les diviseurs spécifiés.                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Modifie la fenêtre pour un contexte de périphérique à l’aide des ratios formés par le multiplicands et les diviseurs spécifiés.                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Convertit les coordonnées d’écran d’un point spécifié sur l’écran en coordonnées clientes.                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | Définit les préférences d’orientation de l’affichage.                                                                                 |
| [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Définit le mode graphique pour le contexte de périphérique spécifié.                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Définit le mode de mappage du contexte de périphérique spécifié.                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Définit les étendues horizontale et verticale de la fenêtre d’affichage pour un contexte de périphérique à l’aide des valeurs spécifiées.                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Spécifie le point d’appareil qui correspond à l’origine de la fenêtre (0,0).                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Définit les étendues horizontale et verticale de la fenêtre pour un contexte de périphérique à l’aide des valeurs spécifiées.                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Spécifie le point de la fenêtre qui est mappé à l’origine de la fenêtre d’affichage (0,0).                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Définit une transformation linéaire à deux dimensions entre l’espace universel et l’espace de page pour le contexte de périphérique spécifié.                |



 

 

 
