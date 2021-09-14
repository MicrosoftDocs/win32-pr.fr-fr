---
title: Fonctionnement du modèle d’objet de texte UI Automation
description: Cette rubrique décrit comment les applications clientes UI Automation Microsoft accèdent au contenu textuel d’un contrôle textuel.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clients, fonctionnement du modèle d’objet de texte UI Automation
- clients, contrôles textuels
- clients, plages de texte
- clients, modèle de contrôle de texte
- clients, modèle de contrôle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292458"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Fonctionnement du modèle d’objet de texte UI Automation

Cette rubrique décrit comment les applications clientes UI Automation Microsoft accèdent au contenu textuel d’un contrôle textuel.

-   [Modèle d’objet spécifique au contrôle](#control-specific-object-model)
-   [Rubriques connexes](#related-topics)

Les contrôles textuels exposent du contenu textuel aux applications clientes UI Automation via un modèle d’objet de texte simple. Les applications clientes ont accès au modèle d’objet de texte par le biais des interfaces de modèle de contrôle [Text et TextRange](uiauto-about-text-and-textrange-patterns.md) , notamment [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) et [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Les applications clientes peuvent utiliser ces interfaces pour récupérer du contenu textuel, des attributs de texte et des objets incorporés, tels que des tables et des liens hypertexte à partir de contrôles textuels.

Les types de contrôle qui prennent en charge le modèle d’objet de texte UI Automation incluent les types de contrôle de [modification](uiauto-supporteditcontroltype.md) et de [document](uiauto-supportdocumentcontroltype.md) . D’autres types de contrôle comme [info-bulle](uiauto-supporttooltipcontroltype.md) et [texte](uiauto-supporttextcontroltype.md) peuvent également prendre en charge le modèle d’objet de texte, mais ils ne sont pas requis pour.

> [!Note]  
> Le modèle d’objet de texte UI Automation n’offre aucun moyen d’insérer ou de modifier du texte. Toutefois, certains contrôles permettent l’insertion ou la modification de texte par le biais de l’interface [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) , ou via une entrée directe au clavier.

 

## <a name="control-specific-object-model"></a>Modèle d’objet spécifique au contrôle

Un contrôle basé sur du texte qui implémente son propre Document Object Model (DOM) peut exposer le DOM en implémentant le modèle de contrôle [ObjectModel](uiauto-implementingobjectmodel.md) . L’exposition du DOM peut permettre aux applications clientes d’accéder plus ou plus au contenu d’un contrôle textuel.

Une application cliente peut découvrir si un contrôle textuel particulier implémente un DOM en extrayant l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) du contrôle. Ensuite, appelez la méthode [**IUIAutomationElement :: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , en spécifiant l’identificateur de propriété [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) et un variant qui reçoit la valeur true si le contrôle implémente un DOM.

Pour accéder au DOM, appelez la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , en spécifiant l’identificateur de modèle de contrôle [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) et une variable qui reçoit l’interface [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) . Appelez la méthode [**IUIAutomationObjectModelPattern :: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) pour récupérer l’interface DOM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de contrôle Text et TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




