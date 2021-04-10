---
title: Compréhension des problèmes liés aux threads
description: Cette rubrique décrit les scénarios courants de Threading pour les implémentations du client Microsoft UI Automation et explique comment éviter les problèmes qui peuvent se produire si un client utilise incorrectement le Threading.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clients, problèmes liés aux threads UI Automation
- clients, problèmes liés aux threads
- clients, modèle de thread du gestionnaire d’événements
- clients, modèle de thread du gestionnaire d’événements UI Automation
- clients, affinité UI Automation
- clients, affinité
- UI Automation, problèmes liés aux threads
- UI Automation, modèle de thread du gestionnaire d’événements
- UI Automation, affinité
- problèmes liés aux threads
- modèle de thread du gestionnaire d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031293"
---
# <a name="understanding-threading-issues"></a>Compréhension des problèmes liés aux threads

Cette rubrique décrit les scénarios courants de Threading pour les implémentations du client Microsoft UI Automation et explique comment éviter les problèmes qui peuvent se produire si un client utilise incorrectement le Threading.

Cette rubrique contient les sections suivantes :

-   [UI Automation et thread d’interface utilisateur](#ui-automation-and-the-ui-thread)
-   [Modèle de thread pour les gestionnaires d’événements](#threading-model-for-event-handlers)
-   [Affinité COM Apartment sur Windows 64 bits](#com-apartment-affinity-on-64-bit-windows)
-   [Rubriques connexes](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>UI Automation et thread d’interface utilisateur

En raison de la façon dont UI Automation utilise les messages Windows, des conflits peuvent se produire lorsqu’une application cliente tente d’interagir avec sa propre interface utilisateur sur le thread d’interface utilisateur. Ces conflits peuvent entraîner des performances très lentes, voire entraîner l’arrêt de la réponse de l’application.

Si votre application cliente est destinée à interagir avec tous les éléments sur le bureau, y compris sa propre interface utilisateur, vous devez effectuer tous les appels UI Automation à partir d’un thread distinct. Cela comprend la localisation d’éléments, par exemple, à l’aide de [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) ou de la méthode [**IUIAutomationElement :: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) et à l’aide de modèles de contrôle. Ce thread ne doit pas posséder de fenêtres. il doit s’agir d’un thread de modèle COM (Component Object Apartment) (MTA), qui initialise COM en appelant [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) avec l’indicateur **coinit \_ multithread** .

Il est possible d’effectuer des appels d’automatisation d’interface utilisateur dans un gestionnaire d’événements UI Automation, car le gestionnaire d’événements est toujours appelé sur un thread autre qu’un thread d’interface utilisateur. Toutefois, lors de l’abonnement à des événements qui peuvent provenir de l’interface utilisateur de votre application cliente, vous devez effectuer l’appel à [**IUIAutomation :: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), ou une méthode associée, sur un thread non-interface utilisateur (qui doit également être un thread MTA). Supprimez les gestionnaires d’événements situés sur un même thread.

Un client UI Automation ne doit pas utiliser plusieurs threads pour ajouter ou supprimer des gestionnaires d’événements. Un comportement inattendu peut se produire si un gestionnaire d’événements est ajouté ou supprimé alors qu’un autre est ajouté ou supprimé dans le même processus client.

## <a name="threading-model-for-event-handlers"></a>Modèle de thread pour les gestionnaires d’événements

Un client UI Automation doit utiliser le modèle de thread MTA COM pour les threads qui implémentent des gestionnaires d’événements. L’utilisation du modèle STA (Single-Threaded Apartment) peut entraîner des problèmes tels que l’empêchement des clients de supprimer des gestionnaires d’événements du thread.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>Affinité COM Apartment sur Windows 64 bits

Selon la spécification COM, la durée de vie d’un objet distant est régie par la durée de vie du cloisonnement dans lequel la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) est appelée pour créer l’objet. Lorsque le cloisonnement d’origine s’arrête, l’objet distant est également libéré.

Pour les clients UI Automation, ce comportement COM peut signifier que la durée de vie du programme d’assistance 32/64 distant (créé par UIAutomationCore.dll) utilisé par un élément 32 bits est régie par la durée de vie cloisonnée du thread qui a créé l’élément. Si le client UI Automation marshale l’élément à un autre thread, l’élément peut devenir invalidé lorsque le cloisonnement d’origine s’arrête. Le client UI Automation doit gérer ces problèmes correctement en interceptant les erreurs lors de l’utilisation d’éléments d’automatisation marshalés.

Le même problème peut se produire avec un client UI Automation 32 bits qui comporte des éléments 64 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Obtention d'éléments UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Abonnement à des événements UI Automation](uiauto-eventsforclients.md)
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[INFORMATIONS : descriptions et travaux des modèles de threads OLE](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 