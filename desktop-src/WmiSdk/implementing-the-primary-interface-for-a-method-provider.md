---
description: 'Un fournisseur de méthodes doit implémenter IWbemServices comme interface principale. Toutefois, un fournisseur de méthode pur requiert uniquement que vous implémentiez la méthode IWbemServices :: ExecMethodAsync.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524340"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a><span data-ttu-id="69266-104">Implémentation de l’interface principale pour un fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="69266-104">Implementing the Primary Interface for a Method Provider</span></span>

<span data-ttu-id="69266-105">Un fournisseur de méthodes doit implémenter [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) comme interface principale.</span><span class="sxs-lookup"><span data-stu-id="69266-105">A method provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="69266-106">Toutefois, un fournisseur de méthode pur requiert uniquement que vous implémentiez la méthode [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .</span><span class="sxs-lookup"><span data-stu-id="69266-106">However, a pure method provider requires only that you implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method.</span></span>

<span data-ttu-id="69266-107">Étant donné que d’autres fournisseurs utilisent [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), l’interface contient de nombreuses méthodes qui ne sont pas pertinentes pour un fournisseur de méthode pur.</span><span class="sxs-lookup"><span data-stu-id="69266-107">Because other providers use [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), the interface contains many methods that are irrelevant to a pure method provider.</span></span> <span data-ttu-id="69266-108">Votre fournisseur de méthode pur doit fournir une implémentation de stub qui retourne le \_ fournisseur WBEM E qui \_ \_ ne \_ peut pas être utilisé pour toutes les autres méthodes **IWbemServices** en plus de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="69266-108">Your pure method provider should supply a stub implementation that returns WBEM\_E\_PROVIDER\_NOT\_CAPABLE for all of other **IWbemServices** methods besides [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span> <span data-ttu-id="69266-109">Toutefois, de nombreux fournisseurs de méthode servent également de fournisseurs d’instances ou de classes.</span><span class="sxs-lookup"><span data-stu-id="69266-109">However, many method providers also serve as instance or class providers.</span></span> <span data-ttu-id="69266-110">La méthode combinée et les fournisseurs d’instances doivent prendre en charge plusieurs méthodes **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="69266-110">Combination method and instance providers must support more of the **IWbemServices** methods.</span></span>

 

 



