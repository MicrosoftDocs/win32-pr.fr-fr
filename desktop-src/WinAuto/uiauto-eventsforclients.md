---
title: Abonnement à des événements UI Automation
description: Microsoft UI Automation permet aux clients de s’abonner à des événements intéressants. Cette fonctionnalité améliore les performances en éliminant la nécessité d’interroger continuellement les éléments de l’interface utilisateur du système pour voir si des informations, une structure ou un État ont été modifiés.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- clients, événements UI Automation
- clients, événements pour UI Automation
- UI Automation, événements pour les clients
- UI Automation, événements clients
- UI Automation, abonnement à des événements
- UI Automation, méthodes d’abonnement
- UI Automation, exemples de code
- UI Automation, exemples
- UI Automation, exemples
- s'abonner à des événements UI Automation
- événements, abonnement UI Automation
- Exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a89df1b9d2afc401e07b6cd77d1307d912f11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310221"
---
# <a name="subscribing-to-ui-automation-events"></a>Abonnement à des événements UI Automation

Microsoft UI Automation permet aux clients de s’abonner à des événements intéressants. Cette fonctionnalité améliore les performances en éliminant la nécessité d’interroger continuellement les éléments de l’interface utilisateur du système pour voir si des informations, une structure ou un État ont été modifiés.

L’efficacité est également améliorée par la possibilité d’écouter des événements uniquement dans une portée définie. Par exemple, un client peut écouter les modifications de sélection d’un élément dans une liste, dans la liste elle-même ou dans une boîte de dialogue entière.

> [!Note]  
> Ne partez pas du principe que tous les événements possibles sont déclenchés par un fournisseur UI Automation. Par exemple, toutes les modifications de propriété n’entraînent pas le déclenchement d’événements par les fournisseurs de proxy standard pour Windows Forms et les contrôles Microsoft Win32.

 

Pour obtenir une vue plus large des événements UI Automation, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).

> [!Note]  
> Avant d’implémenter un gestionnaire d’événements, vous devez vous familiariser avec les problèmes de Threading décrits dans la rubrique [compréhension des problèmes de Threading](uiauto-threading.md).

 

Cette rubrique contient les sections suivantes.

-   [Inscription des gestionnaires d’événements](#registering-event-handlers)
-   [Exemples](#examples)
-   [Rubriques connexes](#related-topics)

## <a name="registering-event-handlers"></a>Inscription des gestionnaires d’événements

Les applications clientes s’abonnent à des événements d’un genre particulier en inscrivant un gestionnaire d’événements, à l’aide de l’une des méthodes [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) suivantes.



| Méthode d’abonnement                                                                                                                                                                                                | Type d'événement       | Interface de rappel                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Modification du focus     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Modification de propriété  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Modification de la structure | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Notification     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Autres événements     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Lorsqu’un client ajoute un gestionnaire d’événements pour tous les descendants ([**TreeScope \_ descendants**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)), UI Automation ajoute un seul gestionnaire pour la racine de la sous-arborescence, et le gestionnaire écoute tous les descendants. UI Automation n’ajoute pas de gestionnaires d’événements de manière récursive.

Lorsqu’un client appelle la méthode [**IUIAutomation :: RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) , UI Automation supprime tous les gestionnaires d’événements du processus client.

Pour recevoir et gérer des événements, vous implémentez un objet de gestion d’événements qui expose une interface de rappel, et vous devez inscrire l’objet en appelant une méthode d’inscription d’événement telle que [**IUIAutomation :: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). L’interface de rappel a une seule méthode ; UI Automation appelle cette méthode lorsque l’événement est traité.

Lors de l’arrêt, ou lorsque les événements UI Automation ne sont plus intéressants pour l’application, les clients UI Automation doivent appeler une ou plusieurs des méthodes [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) suivantes.

> [!Note]  
> Un client UI Automation ne doit pas utiliser plusieurs threads pour ajouter ou supprimer des gestionnaires d’événements. Un comportement inattendu peut se produire si un gestionnaire d’événements est ajouté ou supprimé alors qu’un autre est ajouté ou supprimé dans le même processus client.

 



| Méthode                                                                                                | Description                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Annule l’inscription d’un gestionnaire d’événements qui a été inscrit à l’aide de [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Annule l’inscription d’un gestionnaire d’événements qui a été inscrit à l’aide de [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Annule l’inscription d’un gestionnaire d’événements qui a été inscrit à l’aide de [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray). |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Annule l’inscription d’un gestionnaire d’événements qui a été inscrit à l’aide de [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Annule l’inscription d’un gestionnaire d’événements qui Weas inscrit à l’aide de [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Annule l’inscription de tous les gestionnaires d’événements inscrits.                                                                                                                                                                                                                                      |



 

Il est possible qu’un événement soit remis à un gestionnaire d’événements après l’annulation de l’abonnement au gestionnaire, si l’événement est reçu simultanément avec la demande d’annulation de l’abonnement à l’événement. La meilleure pratique consiste à suivre la norme COM (Component Object Model) et à éviter de détruire l’objet de gestionnaire d’événements jusqu’à ce que son décompte de références ait atteint zéro. La destruction d’un gestionnaire d’événements immédiatement après l’annulation de l’abonnement à des événements peut entraîner une violation d’accès si un événement est remis en retard.

## <a name="examples"></a>Exemples

Pour obtenir des exemples de code qui montrent comment gérer des événements UI Automation, consultez [comment implémenter des gestionnaires d’événements](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Compréhension des problèmes liés aux threads](uiauto-threading.md)
</dt> </dl>

 

 




