---
title: Implémentation d’une interface principale de fournisseur d’instance
description: Un fournisseur d’instances utilise les méthodes asynchrones de IWbemServices comme interface principale pour WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541882"
---
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="12c83-103">Implémentation d’une interface principale de fournisseur d’instance</span><span class="sxs-lookup"><span data-stu-id="12c83-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="12c83-104">Un fournisseur d’instances utilise les méthodes asynchrones de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) comme interface principale pour WMI.</span><span class="sxs-lookup"><span data-stu-id="12c83-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="12c83-105">En implémentant uniquement les méthodes qui répondent aux besoins de votre fournisseur d’instance, vous pouvez réduire la quantité de ressources que vous consacrez au codage.</span><span class="sxs-lookup"><span data-stu-id="12c83-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="12c83-106">Toutefois, en implémentant des méthodes réservées pour d’autres types de fournisseurs, vous pouvez réduire le nombre de fournisseurs que vous écrivez.</span><span class="sxs-lookup"><span data-stu-id="12c83-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="12c83-107">Comme il est également utilisé par les applications et les fournisseurs pour demander des services de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contient de nombreuses méthodes qui ne sont pas pertinentes pour un fournisseur d’instances.</span><span class="sxs-lookup"><span data-stu-id="12c83-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="12c83-108">Le tableau suivant répertorie les méthodes **IWbemServices** que vous pouvez implémenter pour un fournisseur d’instances.</span><span class="sxs-lookup"><span data-stu-id="12c83-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="12c83-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="12c83-109">Method</span></span>                                                                   | <span data-ttu-id="12c83-110">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="12c83-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="12c83-111">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="12c83-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="12c83-112">Récupération</span><span class="sxs-lookup"><span data-stu-id="12c83-112">Retrieval</span></span>        |
| [<span data-ttu-id="12c83-113">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="12c83-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="12c83-114">Modification</span><span class="sxs-lookup"><span data-stu-id="12c83-114">Modification</span></span>     |
| [<span data-ttu-id="12c83-115">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="12c83-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="12c83-116">Suppression</span><span class="sxs-lookup"><span data-stu-id="12c83-116">Deletion</span></span>         |
| [<span data-ttu-id="12c83-117">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="12c83-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="12c83-118">Énumération</span><span class="sxs-lookup"><span data-stu-id="12c83-118">Enumeration</span></span>      |
| [<span data-ttu-id="12c83-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="12c83-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="12c83-120">Traitement des requêtes</span><span class="sxs-lookup"><span data-stu-id="12c83-120">Query processing</span></span> |



 

<span data-ttu-id="12c83-121">Pour les méthodes que vous n’utilisez pas, votre fournisseur peut fournir une implémentation de stub qui retourne un **\_ fournisseur WBEM E \_ \_ non \_ capable**.</span><span class="sxs-lookup"><span data-stu-id="12c83-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="12c83-122">Cela comprend toutes les méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) non listées dans le tableau ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="12c83-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="12c83-123">Un fournisseur unique peut agir simultanément en tant que fournisseur de classes, d’instances et de méthodes en effectuant une inscription et une implémentation correctes de toutes les méthodes pertinentes.</span><span class="sxs-lookup"><span data-stu-id="12c83-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="12c83-124">Pour plus d’informations, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md) et [écriture d’un fournisseur de méthodes](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="12c83-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



