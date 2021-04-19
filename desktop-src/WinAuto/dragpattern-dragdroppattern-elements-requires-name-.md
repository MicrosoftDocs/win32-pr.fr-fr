---
title: Les éléments DragPattern/DragDropPattern requièrent un nom
description: Les éléments DragPattern/DragDropPattern requièrent un nom
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511198"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>Les éléments DragPattern/DragDropPattern requièrent un nom

## <a name="text"></a>Texte

Les éléments qui prennent en charge le glisser-déplacer doivent avoir un’name’valide

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

L’élément prend en charge [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mais n’a pas de nom valide défini.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran. L’utilisateur ne sera pas en mesure d’indiquer cet objet, car la lecture de l’écran ne lit pas un nom valide pour distinguer ce que cet élément est en déplacement.

## <a name="possible-causes"></a>Causes possibles

-   L’élément, ou son parent, a un nom ou une étiquette incorrectement attribué.
-   Un développeur ne sait pas que les lecteurs d’écran lisent les noms et les types de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriété Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




