---
description: Si ce bit est défini, la boîte de dialogue est une boîte de dialogue d’erreur.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de style de boîte de dialogue d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091362"
---
# <a name="error-dialog-style-bit"></a>Bit de style de boîte de dialogue d’erreur

Si ce bit est défini, la boîte de dialogue est une boîte de dialogue d’erreur.

Il peut y avoir plusieurs boîtes de dialogue avec ce style. La propriété **ErrorDialog** détermine la boîte de dialogue qui est utilisée comme boîte de dialogue d’erreur. La boîte de dialogue sélectionnée peut être une seule de celles pour lesquelles ce bit de style est défini. La boîte de dialogue d’erreur doit avoir un contrôle de texte statique nommé ErrorText. Ce contrôle reçoit le texte du message d’erreur. La boîte de dialogue doit également comporter les sept boutons de commande correspondant aux valeurs de retour possibles. Le message d’erreur détermine lequel de ces boutons est réellement affiché. Les boutons affichés sont réorganisés de sorte qu’ils sont répartis uniformément dans la boîte de dialogue. Cette réorganisation modifie la coordonnée X des boutons, mais pas les trois autres coordonnées. Par conséquent, il est recommandé qu’aucun autre contrôle ne soit créé dans la même région horizontale de la boîte de dialogue que les boutons. Si le message d’erreur ne spécifie aucun bouton, le bouton **OK** s’affiche. Le bouton **par défaut** , le premier contrôle actif et les valeurs du bouton **Annuler** sont ignorés pour une boîte de dialogue d’erreur. Le bouton **par défaut** défini dans le message d’erreur sera affecté aux trois valeurs. L’effet de l’exécution de ces boutons doit être défini dans la [table ControlEvent,](controlevent-table.md) comme pour tous les autres boutons. Le titre de la boîte de dialogue est créé d’une manière similaire à d’autres boîtes de dialogue. Il peut être remplacé par le message d’erreur s’il spécifie un texte d’en-tête après la liste de boutons.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbDialogAttributesError** |



 

 

 



