---
title: Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide
description: Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670977"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide

## <a name="text"></a>Texte

Les éléments qui prennent en charge le glisser-déplacer doivent avoir un ensemble’DropEffect’valide

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

L’élément prend en charge [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mais ne dispose pas d’un jeu de propriétés [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) valide.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran. L’utilisateur ne sera pas en mesure d’indiquer l’effet de cet objet lors de son déplacement.

## <a name="possible-causes"></a>Causes possibles

-   L’élément, ou son parent, n’a pas créé le [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ou [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un nom ou une étiquette incorrectement assigné.
-   Un développeur ne sait pas que les lecteurs d’écran lisent les DropEffect.

 

 




