---
title: TextEdit (modèle de contrôle)
description: Présente des recommandations et des conventions pour l’implémentation de ITextEditProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- UI Automation, implémenter le modèle de contrôle TextEdit
- UI Automation, modèle de contrôle TextEdit
- modèles de contrôle, TextEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316349"
---
# <a name="textedit-control-pattern"></a>TextEdit (modèle de contrôle)

Présente des recommandations et des conventions pour l’implémentation de [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **TextEdit** est utilisé pour l’accès par programme à un contrôle qui modifie le texte, par exemple un contrôle qui effectue une correction automatique ou active la composition d’entrée.

> [!Note]  
> Les notes d’implémentation de cette rubrique font référence aux API qui proviennent de Text Services Framework (TSF). Pour plus d’informations sur TSF et la référence d’API, consultez [Text Services Framework](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Membres requis pour **ITextEditProvider**

Ces propriétés et méthodes sont requises pour implémenter l’interface [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) .



| Membres nécessaires                                                              | Type de membre | Notes                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Méthode      | Retourne la plage de la conversion actuelle (None s’il n’y a pas de conversion). Retourne la composition active (dans TSF, il s’agit de la plage marquée par la **\_ \_ composition GUID prop**). Par exemple, dans l’éditeur de méthode d’entrée (IME) japonais de Microsoft, il s’agit du texte entièrement souligné. |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Méthode      | Retourne la plage cible de conversion actuelle (None si aucune conversion). Dans TSF, il s’agit de la plage de caractères marqués **tf \_ attr \_ target \_ NOTCONVERTED** ou **tf \_ attr \_ target \_ converti** à partir de la structure **\_ DISPLAYATTRIBUTE TF** .                                               |



 

Les événements **TextEditTextChanged** et **ConversionTargetChanged** doivent être déclenchés par les éléments Microsoft UI Automation qui prennent en charge le modèle **TextEdit** .

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   Utilisez la fonction [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) pour déclencher l’événement **TextEditTextChanged** .
-   Le tableau suivant répertorie les cas où vous devez déclencher l’événement et les paramètres [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) à utiliser.



| TextEditChangeType                                            | Charge utile d'un événement                                | Notes                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Correction automatique**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Nouvelle chaîne corrigée                         | Déclenché lorsqu’une correction automatique est effectuée par le contrôle. Ou chaque fois qu’un remplacement est effectué via TSF et que la plage a une valeur **GUID \_ prop \_ TKB \_ alternatives** de **TKB \_ alternatives la \_ Correction automatique est \_ appliquée**.<br/>                                                                                                                                                                   |
| [**Composition**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Chaîne mise à jour                           | La charge utile ne doit inclure que les caractères qui ont changé (n’envoyez pas la totalité de la chaîne de composition). Déclenché chaque fois qu’un remplacement de composition est effectué. Dans TSF, le remplacement d’une composition est défini comme un remplacement dont l’indicateur de **\_ \_ composition GUID prop** est défini. Les contrôles d’édition qui implémentent TSF peuvent surveiller ces modifications via la notification **OnEndEdit** .<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | La chaîne de composition finalisée (voir les remarques) | Dans TSF, la chaîne de conversion en cours de finalisation est définie par la suppression de l’indicateur de **\_ \_ composition GUID prop** dans une composition. Les contrôles d’édition qui implémentent TSF doivent déterminer la chaîne finalisée de **EndComposition** et déclencher l’événement lorsque **OnEndEdit** est appelé.<br/> La chaîne de composition finalisée peut être vide si la composition a été annulée ou supprimée.<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   **ConversionTargetChanged** se produit lorsque la cible de conversion passe d’une cible à une autre.
-   Utilisez la fonction [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) pour déclencher l’événement **ConversionTargetChanged** (passez l’identificateur d’événement [**UIA \_ TextEdit \_ ConversionTargetChangedEventId**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) ).
-   **ConversionTargetChanged** ne doit pas être déclenché lorsque le contenu de la cible change. Si la modification cible se produit de façon simultanée avec une modification de la composition, l’événement de modification cible doit être déclenché une fois que tous les événements de composition ont déjà été déclenchés.
-   Dans TSF, la cible de conversion est définie par la valeur **tf \_ attr \_ target \_ convertie** définie à partir de la structure **\_ DISPLAYATTRIBUTE TF** . Les modifications peuvent être surveillées à l’aide de **OnEndEdit**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

