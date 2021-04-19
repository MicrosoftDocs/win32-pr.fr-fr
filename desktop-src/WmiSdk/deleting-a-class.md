---
description: Contrairement à la suppression d’une instance dynamique, la suppression d’une classe est une procédure simple.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Suppression d’une classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538698"
---
# <a name="deleting-a-class"></a>Suppression d’une classe

Contrairement à la suppression d’une instance dynamique, la suppression d’une classe est une procédure simple. Toutefois, comme nous l’avons vu précédemment, les classes de base ou dérivées sont rarement supprimées. Au lieu de cela, une instance est plus souvent supprimée. L' [API de script pour WMI](scripting-api-for-wmi.md) utilise les mêmes méthodes pour supprimer un objet de classe ou une instance. Pour plus d’informations, consultez [Suppression d’une instance](deleting-an-instance.md). Pour plus d’informations sur la suppression de classes et d’instances de l’espace de stockage WMI, consultez la commande de préprocesseur [**pragma deleteclass**](pragma-deleteclass.md) .

L' [API com pour WMI](com-api-for-wmi.md) a différentes méthodes pour supprimer une instance et supprimer un objet.

La procédure suivante décrit comment supprimer une classe de base ou une classe dérivée.

**Pour supprimer une classe de base ou une classe dérivée**

-   Appelez la méthode [**IWbemServices ::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) ou [**IWbemServices ::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .

    Comme son nom l’indique, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) supprime une instance de façon asynchrone tandis que [**deleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) supprime une instance de façon synchrone. Pour utiliser **DeleteClassAsync**, vous devez également implémenter un objet [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

 

 



