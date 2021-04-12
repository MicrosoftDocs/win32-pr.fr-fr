---
title: Interfaces de condition de propriété pour les clients
description: Cette section décrit les interfaces de condition de propriété pour les clients UI Automation pour les applications Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031329"
---
# <a name="property-condition-interfaces-for-clients"></a>Interfaces de condition de propriété pour les clients

Cette section décrit les interfaces de condition de propriété pour les clients UI Automation pour les applications Microsoft Win32.

## <a name="in-this-section"></a>Dans cette section



| Interface                                                                                  | Description                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Expose les propriétés et les méthodes que les applications clientes UI Automation de Microsoft peuvent utiliser pour récupérer des informations sur une condition de propriété basée sur et. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Représente une condition qui peut avoir la **valeur true** (sélectionne tous les éléments) ou **false** (ne sélectionne aucun élément).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Il s’agit de l’interface principale pour les conditions utilisées dans le filtrage lors de la recherche d’éléments dans l’arborescence UI Automation.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Représente une condition qui est la valeur négative d’une autre condition.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Représente une condition composée de plusieurs conditions, au moins l’une d’entre elles devant avoir la valeur true.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Représente une condition basée sur une valeur de propriété utilisée pour rechercher des éléments UI Automation.<br/>                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

