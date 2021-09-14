---
description: Types de threads du distributeur de ressources COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Types de threads du distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922960"
---
# <a name="com-resource-dispenser-thread-types"></a>Types de threads du distributeur de ressources COM+

Les appels dans un distributeur de ressources COM+ peuvent provenir de l’un des types de threads suivants :

-   Thread cloisonné (STA)
-   Thread libre (MTA)
-   Thread non-COM (application ou thread de garbage collector du [Gestionnaire de distribution](com--dispenser-manager.md) )

Si un distributeur de ressources n’est pas un objet COM, il doit être en mesure de gérer les appels arrivant à partir de n’importe quel thread à tout moment. Si un distributeur de ressources est un objet COM, l’objet COM doit être inscrit avec un modèle de thread des **deux**. Cela permet aux threads STA ou MTA de créer et d’utiliser le distributeur de ressources sans basculement de thread.

Si un distributeur de ressources crée et utilise un autre objet COM (par exemple, un gestionnaire de ressources hors processus), le distributeur de ressources peut avoir besoin de gérer plusieurs proxies vers cet autre objet COM et de s’assurer que les appels à l’objet sont effectués à l’aide du proxy approprié pour le thread appelant. Lorsque le distributeur de ressources crée cet objet, il marshale et enregistre la référence. Avant d’appeler à nouveau l’objet, il doit être démarshalé pour créer un proxy pour le thread appelant.

Il peut être plus efficace de mettre en cache ces proxys par thread en conservant un mappage de l’ID de thread à un pointeur proxy. Ce mappage se développe à mesure que de nouveaux threads sont utilisés dans le processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



