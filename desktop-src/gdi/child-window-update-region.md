---
description: Une fenêtre enfant est une fenêtre avec le \_ style WS Child ou WS \_ CHILDWINDOW.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Zone de mise à jour de la fenêtre enfant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf702855e506424a08e5be6c6b0cfe514035f1c54348306475140fb7fc440a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105894"
---
# <a name="child-window-update-region"></a>Zone de mise à jour de la fenêtre enfant

Une fenêtre enfant est une fenêtre avec le \_ style WS Child ou WS \_ CHILDWINDOW. Comme les autres styles de fenêtre, les fenêtres enfants reçoivent des messages de [**\_ peinture WM**](wm-paint.md) pour demander une mise à jour. Chaque fenêtre enfant a une région de mise à jour, que le système ou l’application peut définir pour générer des messages de **\_ peinture WM** éventuels.

Les régions visibles et mises à jour d’une fenêtre enfant sont affectées par la fenêtre parente de l’enfant ; Cela n’est pas vrai pour les fenêtres d’autres styles. Le système définit souvent la région de mise à jour de la fenêtre enfant lorsqu’elle définit la région de mise à jour de la fenêtre parente, ce qui amène la fenêtre enfant à recevoir les messages de [**\_ peinture WM**](wm-paint.md) lorsque la fenêtre parente les reçoit. Le système limite l’emplacement de la zone visible de la fenêtre enfant à dans la zone cliente de la fenêtre parente et découpe toute partie de la fenêtre enfant déplacée en dehors de la fenêtre parente.

Le système définit la région de mise à jour pour une fenêtre enfant lorsqu’une partie de la région de mise à jour de la fenêtre parente comprend une partie de la fenêtre enfant. Dans ce cas, le système envoie d’abord un message de [**\_ peinture WM**](wm-paint.md) à la fenêtre parente, puis envoie un message à la fenêtre enfant, ce qui permet à l’enfant de restaurer toutes les parties de la fenêtre sur lesquelles le parent peut avoir été dessiné.

Le système ne définit pas la région de mise à jour du parent lorsque la valeur de l’enfant est définie. Une application ne peut pas générer un message de [**\_ peinture WM**](wm-paint.md) pour la fenêtre parente en invalidant la fenêtre enfant. De même, une application ne peut pas générer un message de **\_ peinture WM** pour l’enfant en invalidant une partie de la zone cliente du parent qui se trouve entièrement sous la fenêtre enfant. Dans ce cas, aucune fenêtre ne reçoit un message de **\_ peinture WM** .

Une application peut empêcher la définition de la région de mise à jour d’une fenêtre enfant lorsque la fenêtre parente est définie en spécifiant le \_ style WS CLIPCHILDREN lors de la création de la fenêtre parente. Quand ce style est défini, le système exclut les fenêtres enfants de la région visible du parent et ignore donc toutes les parties de la région de mise à jour qui peuvent contenir les fenêtres enfants. Lorsque l’application peint dans la fenêtre parente, tout dessin qui couvre la fenêtre enfant est coupé, ce qui rend un message de [**\_ peinture WM**](wm-paint.md) ultérieur à la fenêtre enfant inutile.

Les régions de mise à jour et visibles d’une fenêtre enfant sont également affectées par les frères de la fenêtre enfant. Les fenêtres sœurs sont toutes les fenêtres qui ont une fenêtre parente commune. Si les fenêtres sœurs se chevauchent, la définition de la région de mise à jour pour une affecte la région de mise à jour d’une autre, ce qui entraîne l’envoi des messages [**WM \_ Paint**](wm-paint.md) aux deux fenêtres. Si une fenêtre de la chaîne parente est composite (une fenêtre avec WX \_ ex \_ composite), les fenêtres sœurs reçoivent des messages de **\_ peinture WM** dans l’ordre inverse de leur position dans l’ordre de plan. À partir de cela, la fenêtre la plus élevée dans l’ordre de plan (en haut) reçoit son message de **\_ peinture WM** , et vice versa. Si une fenêtre de la chaîne parente n’est pas composite, les fenêtres sœurs reçoivent des messages de **\_ peinture WM** dans l’ordre Z.

Les fenêtres sœurs ne sont pas automatiquement découpées. Un frère peut dessiner sur un autre frère qui se chevauche, même si la fenêtre dessinée a une position inférieure dans l’ordre de plan. Une application peut empêcher cela en spécifiant le \_ style WS CLIPSIBLINGS lors de la création des fenêtres. Quand ce style est défini, le système exclut toutes les parties d’une fenêtre sœur qui se chevauchent de la région visible d’une fenêtre si la fenêtre sœur qui se chevauche a une position supérieure dans l’ordre de plan.

> [!Note]  
> Les régions mises à jour et visibles pour les fenêtres qui ont le \_ style WS Popup ou WS \_ POPUPWINDOW ne sont pas affectées par leurs fenêtres parentes.

 

 

 



