---
title: Gestionnaires d’événements ambiants
description: Gestionnaires d’événements ambiants
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Apparences du lecteur Windows Media, gestionnaires d’événements ambiants
- apparences, gestionnaires d’événements ambiants
- informations de référence sur les apparences, les gestionnaires d’événements ambiants
- gestionnaires d’événements ambiants
- événements, ambiant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379719"
---
# <a name="ambient-event-handlers"></a>Gestionnaires d’événements ambiants

Les gestionnaires d’événements suivants peuvent être implémentés pour la plupart des éléments d’apparence. Les attributs d’événement ambiant accessibles avec le mot clé **Event** peuvent être utilisés dans un gestionnaire d’événements pour déterminer l’état du clavier et de la souris au moment de l’événement.



| Gestionnaire d'événements                                   | Description                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*attribut* \_ changement](attribute-onchange.md) | Lorsqu’un attribut d’apparence change de valeur, un événement qui peut être géré par un gestionnaire d’événements se produit. Le nom du gestionnaire d’événements est le nom de l’attribut suivi d’un trait de soulignement et de « OnChange », tels que « valeur \_ OnChange ». |
| [onblur](onblur.md)                            | Gère un événement qui se produit lorsque l’élément perd le focus clavier.                                                                                                                                                       |
| [OnClick](onclick.md)                          | Gère un événement qui se produit lorsque l’utilisateur clique sur l’élément.                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | Gère un événement qui se produit lorsque l’utilisateur double-clique sur l’élément.                                                                                                                                                         |
| [onendalphablend](onendalphablend.md)          | Gère un événement qui se produit lorsqu’un élément termine une opération **alphaBlendTo** .                                                                                                                                         |
| [onendmove](onendmove.md)                      | Gère un événement qui se produit lorsqu’un élément termine une opération **MoveTo** .                                                                                                                                                |
| [onfocus](onfocus.md)                          | Gère un événement qui se produit lorsque l’élément reçoit le focus clavier.                                                                                                                                                    |
| [OnKeyDown](onkeydown.md)                      | Gère un événement qui se produit lorsqu’une touche est enfoncée.                                                                                                                                                                           |
| [OnKeyPress](onkeypress.md)                    | Gère un événement qui se produit lorsque l’utilisateur appuie sur une touche alphanumérique.                                                                                                                                                       |
| [OnKeyUp](onkeyup.md)                          | Gère un événement qui se produit lorsqu’une touche est relâchée.                                                                                                                                                                          |
| [OnMouseDown](onmousedown.md)                  | Gère un événement qui se produit lorsque l’utilisateur clique sur un bouton de la souris.                                                                                                                                                             |
| [OnMouseMove](onmousemove.md)                  | Gère un événement qui se produit lorsque l’utilisateur déplace le pointeur de la souris pendant qu’il se trouve sur un élément.                                                                                                                               |
| [onmouseout](onmouseout.md)                    | Gère un événement qui se produit lorsque l’utilisateur déplace le pointeur hors de l’élément.                                                                                                                                                 |
| [onmouseover](onmouseover.md)                  | Gère un événement qui se produit lorsque l’utilisateur place d’abord le pointeur sur l’élément.                                                                                                                                         |
| [OnMouseUp](onmouseup.md)                      | Gère un événement qui se produit lorsque l’utilisateur relâche un bouton de la souris alors que le pointeur se trouve sur l’élément.                                                                                                                     |
| [OnResize](onresize.md)                        | Gère un événement qui se produit lorsqu’un contrôle est redimensionné.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’événement ambiant**](ambient-event-attributes.md)
</dt> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




