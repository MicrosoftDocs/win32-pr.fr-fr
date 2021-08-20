---
title: Vue d’ensemble des clients UI Automation
description: Cette rubrique décrit les principales tâches impliquées dans l’implémentation d’une application cliente Microsoft UI Automation.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- UI Automation, vue d’ensemble des clients
- clients, à propos de
- clients, éléments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37ff185e72c25f5c3b8eeba8cdd4ae9250391a867538ad3e4b6de4f8d1dce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928681"
---
# <a name="ui-automation-clients-overview"></a>Vue d’ensemble des clients UI Automation

Cette rubrique décrit les principales tâches impliquées dans l’implémentation d’une application cliente Microsoft UI Automation.

Un client UI Automation est une application qui utilise l’API UI Automation pour accéder aux informations sur les éléments d’interface utilisateur ou pour contrôler les applications par le biais de la manipulation par programmation de leurs éléments d’interface utilisateur. Les clients UI Automation incluent des applications de technologie d’assistance, telles que les lecteurs d’écran, qui récupèrent des informations sur les éléments d’interface utilisateur et présentent les informations de manière utilisable pour les personnes handicapées. Elles incluent également des applications telles que les programmes de reconnaissance vocale et les outils de test de logiciels, qui utilisent UI Automation au lieu de la souris et du clavier pour « piloter » d’autres applications.

Du point de vue d’UI Automation, les principales tâches qu’une application cliente UI Automation doit effectuer sont les suivantes :

1.  **Obtenez une instance de l’objet CUIAutomation.**

    Les informations sur les éléments d’interface utilisateur et l’accès aux fonctionnalités des éléments d’interface utilisateur sont exposées aux clients par les fournisseurs UI Automation. Toutefois, les applications clientes ne fonctionnent pas directement avec les fournisseurs. Au lieu de cela, un service principal se trouve entre le client et le fournisseur. Lorsqu’un client appelle l’API UI Automation, il appelle en fait le service noyau UI Automation qui, à son tour, appelle les interfaces implémentées par le fournisseur.

    Pour accéder au service d’automatisation d’interface utilisateur de base, un client doit créer une instance de l’objet [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) et récupérer un pointeur d’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) sur l’objet. Le pointeur **IUIAutomation** est la clé du client pour accéder à toutes les fonctionnalités d’automatisation d’interface utilisateur disponibles pour le client. Pour plus d’informations, consultez [création de l’objet CUIAutomation](uiauto-creatingcuiautomation.md).

2.  **Récupérez les interfaces IUIAutomationElement pour les éléments d’interface utilisateur à partir de l’arborescence UI Automation.**

    UI Automation expose des éléments d’interface utilisateur individuels comme des objets qui implémentent l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Les informations relatives à un élément sont disponibles pour les clients via des propriétés exposées par l’interface **IUIAutomationElement** de l’élément, ainsi que l’accès aux modèles de contrôle de l’élément. Les propriétés et les méthodes exposées par les interfaces de modèle de contrôle fournissent un accès aux informations et aux fonctionnalités spécifiques au contrôle.

    Les objets d’élément UI Automation sont fournis aux clients dans une arborescence hiérarchique appelée arborescence UI Automation. Les clients utilisent des méthodes exposées par l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) pour récupérer des interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour les éléments d’interface utilisateur dans l’arborescence et pour récupérer d’autres interfaces utilisées pour rechercher dans l’arborescence des éléments qui correspondent à un ensemble de critères spécifique. Pour plus d’informations, consultez [obtention d’éléments UI Automation](uiauto-obtainingelements.md).

    Lors de la récupération des éléments d’interface utilisateur, les clients peuvent améliorer les performances du système en utilisant les fonctionnalités de mise en cache d’UI Automation. La mise en cache permet à un client de spécifier un ensemble de propriétés et de modèles de contrôle à récupérer avec l’élément. Dans un seul appel interprocessus, UI Automation récupère l’élément ainsi que les propriétés et les modèles de contrôle spécifiés, puis les stocke dans le cache. Sans mise en cache, un appel distinct InterProcess est requis pour récupérer chaque modèle de propriété ou de contrôle. Pour plus d’informations, consultez [Caching UI Automation Properties and Control patterns](uiauto-cachingforclients.md).

3.  **Récupérez les propriétés des éléments d’interface utilisateur et appelez les fonctionnalités des éléments d’interface utilisateur.**

    Les clients utilisent l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour récupérer les propriétés et les modèles de contrôle d’un élément. L’interface comprend deux versions de chaque méthode de récupération de propriété : une version récupère la propriété à partir du cache, l’autre récupère la propriété auprès du fournisseur. Pour plus d’informations, consultez [récupération de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).

4.  **Répondre aux événements UI Automation.**

    Les fournisseurs UI Automation notifient les clients des modifications ou des occurrences importantes dans l’interface utilisateur en déclenchant des événements. Les clients doivent déterminer les événements dont ils ont besoin, puis implémenter et inscrire les interfaces de gestion des événements pour recevoir et traiter ces événements. Pour plus d’informations, consultez [abonnement à des événements UI Automation](uiauto-eventsforclients.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 