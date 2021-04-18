---
title: Modèle de contrôle SynchronizedInput
description: Fournit des instructions et des conventions pour l’implémentation de ISynchronizedInputProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- UI Automation, implémentation du modèle de contrôle SynchronizedInput
- UI Automation, modèle de contrôle SynchronizedInput
- UI Automation, ISynchronizedInputProvider
- ISynchronizedInputProvider
- implémentation des modèles de contrôle SynchronizedInput d’UI Automation
- Modèles de contrôle SynchronizedInput
- modèles de contrôle, ISynchronizedInputProvider
- modèles de contrôle, implémenter des SynchronizedInput UI Automation
- modèles de contrôle, SynchronizedInput
- interfaces, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511842"
---
# <a name="synchronizedinput-control-pattern"></a>Modèle de contrôle SynchronizedInput

Fournit des instructions et des conventions pour l’implémentation de [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **SynchronizedInput** permet aux applications clientes UI Automation de Microsoft de diriger l’entrée de la souris ou du clavier vers un élément d’interface utilisateur spécifique.

Ce modèle de contrôle est généralement utilisé dans les scripts de test automatisés pour envoyer une entrée de souris ou de clavier à un élément spécifique de l’interface utilisateur, puis vérifier que l’élément a reçu l’entrée.

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **SynchronizedInput** , notez les conventions et recommandations suivantes :

-   Quand la méthode [**ISynchronizedInputProvider :: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) est appelée, le fournisseur UI Automation doit commencer à vérifier l’entrée du type spécifié, puis effectuer l’une des actions suivantes :
    -   Lorsque l’entrée correspondante est trouvée pour l’élément, le fournisseur doit déclencher l’événement [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) .
    -   Lorsque l’entrée correspondante est trouvée, mais qu’elle a atteint un autre élément, le fournisseur doit déclencher l’événement [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md) .
    -   Si une entrée incompatible est trouvée, le fournisseur doit ignorer l’entrée et déclencher l’événement [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md) .
-   Le fournisseur UI Automation doit ignorer l’entrée s’il s’agit d’un élément autre que l’élément actuel.
-   Lorsque l’élément reçoit l’entrée, ou lorsque la méthode [**ISynchronizedInputProvider :: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) est appelée, le fournisseur arrête la vérification de l’entrée et se poursuit normalement.
-   Si [**ISynchronizedInputProvider :: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) est appelé alors que le fournisseur est déjà à l’écoute de l’entrée, le fournisseur doit retourner [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Membres requis pour **ISynchronizedInputProvider**

Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .



| Membres nécessaires                                                                         | Type de membre | Notes |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Méthode      | Aucun  |
| [**Annuler**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Méthode      | Aucun  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | Événement       | Aucun  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




