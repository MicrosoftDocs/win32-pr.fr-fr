---
title: Vue d'ensemble des événements UI Automation
description: La notification d’événements Microsoft UI Automation est une fonctionnalité clé pour les technologies d’assistance, telles que les lecteurs d’écran et les loupes d’écran.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- UI Automation, vue d’ensemble des événements
- UI Automation, catégories d’événements
- UI Automation, notifications d’événements
- notifications d'événements
- événements, catégories
- événements, notifications d’événements
- Événements de modification de propriété
- Événements d’action d’élément
- Événements de modification de structure
- Événements de modification globaux du Bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010523"
---
# <a name="ui-automation-events-overview"></a>Vue d'ensemble des événements UI Automation

La notification d’événements Microsoft UI Automation est une fonctionnalité clé pour les technologies d’assistance, telles que les lecteurs d’écran et les loupes d’écran. Ces clients UI Automation suivent les événements déclenchés par les fournisseurs UI Automation quand un événement se produit dans l’interface utilisateur et utilisent les informations pour notifier les utilisateurs finaux.

L'efficacité est améliorée en permettant aux applications fournisseurs de déclencher des événements de manière sélective, selon que des clients sont abonnés à ces événements ou non, si aucun client n'écoute d'événement.

Les événements UI Automation s’inscrivent dans les catégories suivantes.



| Catégorie d'événement        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modification de propriété       | Déclenché en cas de modification d’une propriété sur l’élément UI Automation ou le modèle de contrôle. Par exemple, si un client doit surveiller un contrôle de case à cocher d’application, il peut s’inscrire pour écouter un événement de modification de propriété sur la propriété [**IUIAutomationTogglePattern :: CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) . Quand le contrôle de case à cocher est coché ou décoché, le fournisseur déclenche l'événement et le client peut agir de manière appropriée. |
| Action d'élément        | Déclenché lorsqu’une modification de l’interface utilisateur résulte de l’utilisateur final ou de l’activité de programmation, par exemple, lorsque l’utilisateur clique sur un bouton ou l’appelle via [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Modification de la structure      | Déclenché quand la structure de l’arborescence UI Automation change. La structure évolue quand de nouveaux éléments de l’interface utilisateur deviennent visibles, sont masqués ou sont supprimés sur le Bureau.                                                                                                                                                                                                                                                                                                              |
| Modification globale du bureau | Déclenché quand des actions d'intérêt global pour le client se produisent, par exemple quand le focus passe d'un élément à un autre ou qu'une fenêtre se ferme.                                                                                                                                                                                                                                                                                                                      |
| Notification          | Déclenché quand une application appelle la fonction [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) . [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indique le type de la notification.                                                                                                                                                                                                                                                 |



 

Certains événements ne signifient pas nécessairement que l'état de l'interface utilisateur a changé. Par exemple, si l’utilisateur passe à un champ d’entrée de texte, puis clique sur un bouton pour mettre à jour le champ, un événement de [**\_ \_ TextChangedEventId de texte UIA**](uiauto-event-ids.md) est déclenché, même si l’utilisateur n’a pas réellement modifié le texte. Pendant le traitement d'un événement, une application cliente peut être amenée à vérifier ce qui a réellement changé avant d'agir.

Les événements suivants peuvent être déclenchés même quand l'état de l'interface utilisateur n'a pas changé.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (selon la propriété qui a été modifiée)
-   [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)
-   [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)
-   [**\_TextChangedEventId de texte UIA \_**](uiauto-event-ids.md)

Pour obtenir une description de tous les événements UI Automation, consultez [identificateurs d’événements](uiauto-event-ids.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Abonnement à des événements UI Automation](uiauto-eventsforclients.md)
</dt> </dl>

 

 