---
title: Mise en cache des propriétés UI Automation et des modèles de contrôle
description: Lorsque vous utilisez l’automatisation d’interface utilisateur de Microsoft, les clients doivent souvent récupérer plusieurs propriétés pour plusieurs éléments Automation.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- mise en cache, propriétés UI Automation
- mise en cache, propriétés
- mise en cache, modèles de contrôle UI Automation
- mise en cache, modèles de contrôle
- UI Automation, propriétés de mise en cache
- UI Automation, mise en cache des propriétés
- clients, mise en cache des propriétés UI Automation
- clients, mise en cache des modèles de contrôle UI Automation
- UI Automation, mise en cache des modèles de contrôle
- UI Automation, mise en cache du modèle de contrôle
- modèles de contrôle, mise en cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f75a7dc9491565fdfdc0ecc73808c2fb6a9d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379756"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Mise en cache des propriétés UI Automation et des modèles de contrôle

Lorsque vous utilisez l’automatisation d’interface utilisateur de Microsoft, les clients doivent souvent récupérer plusieurs propriétés pour plusieurs éléments Automation. Un client peut récupérer des propriétés individuelles un élément à la fois à l’aide des méthodes de récupération de propriété telles que [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) ou [**CurrentAccessKey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey). Toutefois, cette méthode est lente et inefficace, car elle nécessite un appel inter-processus pour chaque propriété en cours de récupération. Pour améliorer les performances, les clients peuvent utiliser les fonctionnalités de mise en cache (également appelées extraction en bloc) d’UI Automation. La mise en cache permet à un client de récupérer toutes les propriétés souhaitées pour tous les éléments souhaités à l’aide d’un seul appel de méthode. Le client peut ensuite récupérer les propriétés individuelles du cache en fonction des besoins et peut obtenir régulièrement un nouvel instantané du cache, généralement en réponse à des événements qui indiquent des modifications dans l’interface utilisateur.

L’application peut demander la mise en cache lorsqu’elle récupère un élément UI Automation à l’aide d’une méthode, telle que [**IUIAutomation :: ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache), [**IUIAutomationTreeWalker :: GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)ou [**IUIAutomationElement :: FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache).

La mise en cache se produit également lorsque vous spécifiez une requête de cache lors de l’abonnement à des événements. L’élément UI Automation passé à votre gestionnaire d’événements comme source d’un événement contient les propriétés mises en cache et les modèles de contrôle spécifiés par la requête de cache. Toute modification apportée à la demande de cache après vous être abonné à l’événement n’a aucun effet.

Cette rubrique contient les sections suivantes.

-   [Demandes de cache](#cache-requests)
    -   [Spécification de la propriété et des modèles de contrôle à mettre en cache](#specifying-property-and-control-patterns-to-cache)
    -   [Spécification de l’étendue et du filtrage d’une demande de mise en cache](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Force des références d’élément](#strength-of-element-references)
-   [Récupération des enfants et des parents mis en cache](#retrieving-cached-children-and-parents)
-   [Récupération d’un nouvel instantané du cache](#retrieving-a-new-snapshot-of-the-cache)
-   [Exemples](#examples)
-   [Rubriques connexes](#related-topics)

## <a name="cache-requests"></a>Demandes de cache

La mise en cache implique de déterminer les propriétés à récupérer et les éléments à partir desquels les récupérer, puis d’utiliser ces informations pour créer une demande de cache. Chaque fois que le client obtient une interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour l’élément d’interface utilisateur, UI Automation met en cache les informations spécifiées dans la requête de cache.

Pour créer une demande de cache, commencez par utiliser la méthode [**IUIAutomation :: CreateCacheRequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) pour récupérer un pointeur d’interface [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) . Ensuite, configurez la demande de cache à l’aide des méthodes de **IUIAutomationCacheRequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Spécification de la propriété et des modèles de contrôle à mettre en cache

Vous pouvez spécifier des propriétés à mettre en cache en appelant [**IUIAutomationCacheRequest :: AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty). Vous pouvez spécifier des modèles de contrôle à mettre en cache en appelant [**IUIAutomationCacheRequest :: AddPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern). Lorsqu’un modèle de contrôle est mis en cache, ses propriétés ne sont pas automatiquement mises en cache ; vous devez spécifier les propriétés que vous souhaitez mettre en cache à l’aide de **AddProperty**.

Vous pouvez récupérer une propriété de modèle de contrôle (par exemple, la propriété Value du modèle de contrôle [value](uiauto-implementingvalue.md) ), sans avoir à récupérer le modèle de contrôle entier dans le cache. Vous devez récupérer le modèle de contrôle uniquement si vous devez utiliser une méthode de modèle de contrôle.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Spécification de l’étendue et du filtrage d’une demande de mise en cache

Vous pouvez spécifier les éléments dont vous souhaitez mettre en cache les propriétés et les modèles de contrôle en définissant la propriété [**IUIAutomationCacheRequest :: TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) avant d’utiliser la requête. La portée est relative aux éléments qui sont récupérés par la méthode à laquelle la demande de cache est passée. Par exemple, si vous définissez uniquement [**les \_ enfants TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope), puis récupérez un élément UI Automation, les propriétés et les modèles de contrôle des enfants de cet élément sont mis en cache, mais les propriétés et les modèles de contrôle de l’élément lui-même ne sont pas mis en cache. Pour vous assurer que la mise en cache est effectuée pour l’élément récupéré lui-même, vous devez inclure l' **\_ élément TreeScope** dans la propriété **IUIAutomationCacheRequest :: TreeScope** . Il n’est pas possible de définir l’étendue sur **TreeScope \_ parent** ou l' **\_ ancêtre de TreeScope**. Toutefois, un élément parent peut être mis en cache lorsqu’un élément enfant est mis en cache. Dans cette rubrique, consultez la section Récupération des enfants et des parents mis en cache.

L’étendue de la mise en cache est également affectée par la propriété [**IUIAutomationCacheRequest :: TreeFilter**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) . Par défaut, la mise en cache est effectuée uniquement pour les éléments qui apparaissent dans l’affichage de contrôle de l’arborescence UI Automation. Vous pouvez toutefois modifier cette propriété pour appliquer la mise en cache à tous les éléments ou uniquement aux éléments qui apparaissent dans la vue de contenu.

### <a name="strength-of-element-references"></a>Force des références d’élément

Lorsque vous récupérez un élément Automation, par défaut, vous avez accès à toutes les propriétés et à tous les modèles de contrôle de cet élément, y compris les propriétés et les modèles de contrôle qui n’ont pas été mis en cache. Toutefois, vous pouvez spécifier que la référence à l’élément fait référence aux données mises en cache uniquement, en affectant à la propriété [**IUIAutomationCacheRequest :: AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) la valeur **AutomationElementMode \_ None**. Dans ce cas, vous n’avez pas accès aux propriétés et aux modèles de contrôle non mis en cache des éléments récupérés. Cela signifie que vous ne pouvez pas accéder à des propriétés actuelles telles que [**IUIAutomationElement :: CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) ou récupérer un modèle de contrôle à l’aide de [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern). Sur les modèles de contrôle mis en cache, vous ne pouvez pas appeler des méthodes qui effectuent des actions sur le contrôle, telles que [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Un lecteur d’écran est un exemple d’application qui n’a peut-être pas besoin de références complètes aux objets. il peut prérécupérer les propriétés de nom et de type de contrôle des éléments dans une fenêtre sans avoir besoin des objets d’élément Automation eux-mêmes.

## <a name="retrieving-cached-children-and-parents"></a>Récupération des enfants et des parents mis en cache

Lorsque vous récupérez un élément Automation et demandez la mise en cache pour les enfants de cet élément via la propriété [**IUIAutomationCacheRequest :: TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) de la requête, il est possible d’obtenir les éléments enfants en appelant [**IUIAutomationElement :: GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) sur l’élément que vous avez récupéré.

Si [**l' \_ élément TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) est inclus dans l’étendue de la demande de cache, l’élément racine de la requête peut être récupéré en appelant [**IUIAutomationElement :: GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) sur l’un des éléments enfants.

> [!Note]  
> Vous ne pouvez pas mettre en cache les parents ou les ancêtres de l’élément racine de la requête.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Récupération d’un nouvel instantané du cache

Le cache est valide uniquement tant que rien ne change dans l’interface utilisateur. Votre application est chargée de récupérer un nouvel instantané du cache, en général, en réponse aux événements.

Si vous vous abonnez à un événement à l’aide d’une requête de cache, vous obtenez un nouvel instantané [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) du cache comme source de l’événement chaque fois que votre gestionnaire d’événements est appelé. Vous pouvez également récupérer un nouvel instantané des informations mises en cache pour un élément en appelant [**IUIAutomationElement :: BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache). Vous pouvez transmettre le [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) d’origine pour obtenir un nouvel instantané de toutes les informations précédemment mises en cache.

La récupération d’un nouvel instantané du cache ne modifie pas les propriétés des références [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) existantes.

## <a name="examples"></a>Exemples

Pour obtenir des exemples de code qui montrent comment utiliser les fonctionnalités de mise en cache d’UI Automation, consultez Utilisation de la [mise en cache](uiauto-howto-use-caching.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Obtention d'éléments UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> </dl>

 

 




