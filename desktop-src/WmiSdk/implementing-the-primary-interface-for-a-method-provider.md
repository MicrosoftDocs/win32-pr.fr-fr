---
description: 'Un fournisseur de méthodes doit implémenter IWbemServices comme interface principale. Toutefois, un fournisseur de méthode pur requiert uniquement que vous implémentiez la méthode IWbemServices :: ExecMethodAsync.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fcc698155ad0a9e786636045654b08d1cd2b7dfabd946b2d3ee9e8192485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244229"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implémentation de l’interface principale pour un fournisseur de méthode

Un fournisseur de méthodes doit implémenter [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) comme interface principale. Toutefois, un fournisseur de méthode pur requiert uniquement que vous implémentiez la méthode [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .

Étant donné que d’autres fournisseurs utilisent [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), l’interface contient de nombreuses méthodes qui ne sont pas pertinentes pour un fournisseur de méthode pur. Votre fournisseur de méthode pur doit fournir une implémentation de stub qui retourne le \_ fournisseur WBEM E qui \_ \_ ne \_ peut pas être utilisé pour toutes les autres méthodes **IWbemServices** en plus de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). Toutefois, de nombreux fournisseurs de méthode servent également de fournisseurs d’instances ou de classes. La méthode combinée et les fournisseurs d’instances doivent prendre en charge plusieurs méthodes **IWbemServices** .

 

 



