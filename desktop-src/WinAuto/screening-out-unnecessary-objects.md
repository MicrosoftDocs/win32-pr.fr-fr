---
title: Filtrage des objets inutiles
description: Si vous utilisez Inspect pour examiner un contrôle simple comme un bouton de commande OK dans l’accessoire Microsoft WordPad, vous pouvez voir que ces objets de fenêtre parente contiennent également plusieurs objets enfants invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c52dc54f2c32be3aff3e535427668943cf1ee21423636e3be8c018f6e3257b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745282"
---
# <a name="screening-out-unnecessary-objects"></a>Filtrage des objets inutiles

Si vous utilisez [Inspect](inspect-objects.md) pour examiner un contrôle simple comme un bouton de commande OK dans l’accessoire Microsoft WordPad, vous pouvez voir que ces objets de fenêtre parente contiennent également plusieurs objets enfants invisibles. Ces objets invisibles ont le même nom de classe de fenêtre que le contrôle et la [propriété État](state-property.md) du [**système d’État est \_ \_ invisible**](object-state-constants.md). Le tableau suivant répertorie les objets enfants invisibles que Microsoft Active Accessibility crée pour le contrôle.



| Nom          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| Requise      | [**barre de menus du \_ système de rôle \_**](object-roles.md)     | 0          |
| None          | [**\_TITLEBAR système de rôle \_**](object-roles.md)   | 5          |
| Oeuvre | [**barre de menus du \_ système de rôle \_**](object-roles.md)     | 0          |
| Barr    | [**\_ScrollBar système de rôle \_**](object-roles.md) | 5          |
| Horizontal  | [**\_ScrollBar système de rôle \_**](object-roles.md) | 5          |
| « Dimensionner la zone »    | [**\_poignée du système de rôle \_**](object-roles.md)           | 0          |



 

Les développeurs clients doivent identifier et filtrer ces objets de fenêtre parente et les objets enfants invisibles, car ils ne fournissent pas d’informations significatives aux utilisateurs finaux.

 

 




