---
title: Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide
description: Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115677"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide

## <a name="text"></a>Texte

Les éléments qui prennent en charge le glisser-déplacer doivent avoir un ensemble’DropEffect’valide

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

L’élément prend en charge [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mais ne dispose pas d’un jeu de propriétés [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) valide.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran. L’utilisateur ne sera pas en mesure d’indiquer l’effet de cet objet lors de son déplacement.

## <a name="possible-causes"></a>Causes possibles

-   L’élément, ou son parent, n’a pas créé le [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ou [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un nom ou une étiquette incorrectement assigné.
-   Un développeur ne sait pas que les lecteurs d’écran lisent les DropEffect.

 

 




