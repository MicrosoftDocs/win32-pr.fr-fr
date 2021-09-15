---
description: Inscription d’une ressource dans une transaction
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Inscription d’une ressource dans une transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403672"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Inscription d’une ressource dans une transaction

Une fois qu’une ressource a été allouée, mais juste avant de retourner la ressource au distributeur de ressources, le gestionnaire de distribution vérifie avec COM+ pour déterminer si l’objet appelant s’exécute dans une transaction. Si l’objet appelant s’exécute dans une transaction, le gestionnaire du distributeur rappelle le distributeur de ressources et lui demande d’inscrire la ressource dans la transaction. La ressource est ensuite retournée au distributeur de ressources, qui le retourne à l’instance appelante.

Le distributeur de ressources doit pouvoir s’inscrire dans une transaction OLE avec le Distributed Transaction Coordinator (DTC).

> [!Note]  
> L’inscription de la transaction est facultative lorsqu’un distributeur de ressources distribue des ressources non transactionnelles, telles que de la mémoire ou des threads.

 

Lorsqu’une transaction est terminée, COM+ notifie le gestionnaire de distribution qu’il a validé ou abandonné. Ensuite, le gestionnaire de distribution avertit le détenteur de chaque distributeur de ressources que toutes les ressources inscrites dans cette transaction peuvent maintenant être déplacées vers l’inventaire général.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[États des ressources regroupées accessibles au distributeur de ressources COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Processus d’allocation des ressources du distributeur de ressources](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



