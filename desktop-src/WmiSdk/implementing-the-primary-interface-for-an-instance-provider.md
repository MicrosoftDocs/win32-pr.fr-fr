---
title: Implémentation d’une interface principale de fournisseur d’instance
description: Un fournisseur d’instances utilise les méthodes asynchrones de IWbemServices comme interface principale pour WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915759"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Implémentation d’une interface principale de fournisseur d’instance

Un fournisseur d’instances utilise les méthodes asynchrones de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) comme interface principale pour WMI. En implémentant uniquement les méthodes qui répondent aux besoins de votre fournisseur d’instance, vous pouvez réduire la quantité de ressources que vous consacrez au codage. Toutefois, en implémentant des méthodes réservées pour d’autres types de fournisseurs, vous pouvez réduire le nombre de fournisseurs que vous écrivez.

Comme il est également utilisé par les applications et les fournisseurs pour demander des services de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contient de nombreuses méthodes qui ne sont pas pertinentes pour un fournisseur d’instances. Le tableau suivant répertorie les méthodes **IWbemServices** que vous pouvez implémenter pour un fournisseur d’instances.



| Méthode                                                                   | Fonctionnalité          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Récupération        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Modification     |
| [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Suppression         |
| [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Énumération      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Traitement des requêtes |



 

Pour les méthodes que vous n’utilisez pas, votre fournisseur peut fournir une implémentation de stub qui retourne un **\_ fournisseur WBEM E \_ \_ non \_ capable**. Cela comprend toutes les méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) non listées dans le tableau ci-dessus.

Un fournisseur unique peut agir simultanément en tant que fournisseur de classes, d’instances et de méthodes en effectuant une inscription et une implémentation correctes de toutes les méthodes pertinentes. Pour plus d’informations, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md) et [écriture d’un fournisseur de méthodes](writing-a-method-provider.md).

 

 



