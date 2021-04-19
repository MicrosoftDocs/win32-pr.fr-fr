---
title: Filtrage des objets inutiles
description: Si vous utilisez Inspect pour examiner un contrôle simple comme un bouton de commande OK dans l’accessoire Microsoft WordPad, vous pouvez voir que ces objets de fenêtre parente contiennent également plusieurs objets enfants invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510196"
---
# <a name="screening-out-unnecessary-objects"></a>Filtrage des objets inutiles

Si vous utilisez [Inspect](inspect-objects.md) pour examiner un contrôle simple comme un bouton de commande OK dans l’accessoire Microsoft WordPad, vous pouvez voir que ces objets de fenêtre parente contiennent également plusieurs objets enfants invisibles. Ces objets invisibles ont le même nom de classe de fenêtre que le contrôle et la [propriété État](state-property.md) du [**système d’État est \_ \_ invisible**](object-state-constants.md). Le tableau suivant répertorie les objets enfants invisibles que Microsoft Active Accessibility crée pour le contrôle.



| Nom          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| Requise      | [**barre de menus du \_ système de rôle \_**](object-roles.md)     | 0          |
| Aucune          | [**\_TITLEBAR système de rôle \_**](object-roles.md)   | 5          |
| Oeuvre | [**barre de menus du \_ système de rôle \_**](object-roles.md)     | 0          |
| Barr    | [**\_ScrollBar système de rôle \_**](object-roles.md) | 5          |
| Horizontal  | [**\_ScrollBar système de rôle \_**](object-roles.md) | 5          |
| « Dimensionner la zone »    | [**\_poignée du système de rôle \_**](object-roles.md)           | 0          |



 

Les développeurs clients doivent identifier et filtrer ces objets de fenêtre parente et les objets enfants invisibles, car ils ne fournissent pas d’informations significatives aux utilisateurs finaux.

 

 




