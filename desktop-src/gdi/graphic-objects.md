---
description: Le stylet, le pinceau, la bitmap, la palette, la région et le chemin d’accès associés à un contrôleur de périphérique sont appelés objets graphiques. Les attributs suivants sont associés à chacun de ces objets.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Objets graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518504"
---
# <a name="graphic-objects"></a>Objets graphiques

Le stylet, le pinceau, la bitmap, la palette, la région et le chemin d’accès associés à un contrôleur de périphérique sont appelés objets graphiques. Les attributs suivants sont associés à chacun de ces objets.



| Objet graphique | Attributs associés                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Taille, en octets ; Dimensions, en pixels ; format de couleur ; schéma de compression ; et ainsi de suite. |
| Brush          | Style, couleur, motif et origine.                                                  |
| Palette        | Couleurs et taille (ou nombre de couleurs).                                              |
| Police           | Nom de la police, largeur, hauteur, poids, jeu de caractères, etc.                     |
| Chemin d’accès           | Automatiques.                                                                              |
| Stylet            | Style, largeur et couleur.                                                            |
| Région         | Emplacement et dimensions.                                                            |



 

Quand une application crée un contrôleur de réseau, le système stocke automatiquement un ensemble d’objets par défaut dans celui-ci (il n’y a pas de bitmap ou de chemin d’accès par défaut). Une application peut examiner les attributs des objets par défaut en appelant les fonctions [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) et [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . L’application peut modifier ces valeurs par défaut en créant un nouvel objet et en le sélectionnant dans le DC. Un objet est sélectionné dans un DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .

Une application peut définir la couleur de pinceau actuelle sur une valeur de couleur spécifiée avec [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).

La fonction [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) retourne la couleur du pinceau DC. La fonction [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) définit la couleur du stylet sur une valeur de couleur spécifiée. La fonction [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) retourne la couleur du stylet DC.

 

 



