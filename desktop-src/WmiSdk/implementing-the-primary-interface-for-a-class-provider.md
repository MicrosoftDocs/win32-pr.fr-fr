---
description: 'Il existe deux façons d’implémenter un fournisseur de classe : implémentez l’interface en tant que fournisseur de notifications push, ou en tant que fournisseur d’extraction.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319666"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="27b29-103">Implémentation de l’interface principale pour un fournisseur de classes</span><span class="sxs-lookup"><span data-stu-id="27b29-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="27b29-104">Il existe deux façons d’implémenter un fournisseur de classe : implémentez l’interface en tant que fournisseur de notifications push, ou en tant que fournisseur d’extraction.</span><span class="sxs-lookup"><span data-stu-id="27b29-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="27b29-105">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="27b29-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="27b29-106">Implémentation de l’interface principale pour un fournisseur de classes Push</span><span class="sxs-lookup"><span data-stu-id="27b29-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="27b29-107">Implémentation de l’interface principale pour un fournisseur de classe pull</span><span class="sxs-lookup"><span data-stu-id="27b29-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="27b29-108">Implémentation de l’interface principale pour un fournisseur de classes Push</span><span class="sxs-lookup"><span data-stu-id="27b29-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="27b29-109">Tandis que tous les fournisseurs implémentent [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour l’initialisation et au moins une autre interface comme interface principale, un fournisseur Push implémente uniquement **IWbemProviderInit**.</span><span class="sxs-lookup"><span data-stu-id="27b29-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="27b29-110">Assurez-vous que votre implémentation effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="27b29-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="27b29-111">Récupère les données de classe appropriées.</span><span class="sxs-lookup"><span data-stu-id="27b29-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="27b29-112">Place les données dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="27b29-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="27b29-113">Supprime les données obsolètes.</span><span class="sxs-lookup"><span data-stu-id="27b29-113">Deletes obsolete data.</span></span>

<span data-ttu-id="27b29-114">À l’issue du processus d’initialisation, WMI gère toutes les demandes d’application pour les classes appartenant au fournisseur Push sans aucune interaction supplémentaire du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27b29-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="27b29-115">Ensuite, le fournisseur Push agit efficacement comme un client de WMI plutôt qu’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27b29-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="27b29-116">Pour plus d’informations sur l’implémentation de [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), consultez [initialisation d’un fournisseur](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="27b29-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="27b29-117">Lors de l’appel de WMI pour créer, mettre à jour ou supprimer des données dans un fournisseur push, définissez le paramètre *lFlags* pour inclure l’indicateur de **\_ \_ \_ mise à jour du propriétaire de l’indicateur WBEM** dans tous les appels aux méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="27b29-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="27b29-118">Implémentation de l’interface principale pour un fournisseur de classe pull</span><span class="sxs-lookup"><span data-stu-id="27b29-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="27b29-119">Un fournisseur d’extraction de classe doit implémenter [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) en tant qu’interface principale.</span><span class="sxs-lookup"><span data-stu-id="27b29-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="27b29-120">L’interface **IWbemServices** prend en charge la récupération des données, la mise à jour des données, la suppression des données, l’énumération et le traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="27b29-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="27b29-121">Toutefois, étant donné que **IWbemServices** est également utilisé par les applications et les fournisseurs pour demander des services de WMI, **IWbemServices** contient de nombreuses méthodes qui ne sont pas pertinentes pour un fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="27b29-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="27b29-122">Votre implémentation doit prendre en charge la récupération de classe et l’énumération, par le biais des méthodes [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) et [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="27b29-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="27b29-123">Le tableau suivant répertorie les autres méthodes **IWbemServices** asynchrones que vous pouvez implémenter pour un fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="27b29-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="27b29-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="27b29-124">Method</span></span>                                                     | <span data-ttu-id="27b29-125">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="27b29-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="27b29-126">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="27b29-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="27b29-127">Modification</span><span class="sxs-lookup"><span data-stu-id="27b29-127">Modification</span></span> |
| [<span data-ttu-id="27b29-128">**DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="27b29-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="27b29-129">Suppression</span><span class="sxs-lookup"><span data-stu-id="27b29-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="27b29-130">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="27b29-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="27b29-131">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="27b29-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="27b29-132">Votre fournisseur de classe doit fournir une implémentation de stub qui retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** pour toutes les autres méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) qui ne prennent pas en charge votre jeu de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="27b29-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="27b29-133">Plus précisément, WMI ne prend pas en charge le traitement des requêtes pour les fournisseurs de classes.</span><span class="sxs-lookup"><span data-stu-id="27b29-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="27b29-134">Par conséquent, un fournisseur de classe doit retourner le **\_ fournisseur WBEM E qui n’est pas en \_ \_ \_ mesure** de son implémentation de [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), définir sa propriété d’inscription **QuerySupportLevels** sur **null**, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="27b29-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="27b29-135">Les interfaces implémentées par un fournisseur de classes sont très similaires aux interfaces d’un fournisseur d’instances et d’un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="27b29-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="27b29-136">En fait, un seul fournisseur peut agir comme les trois types de fournisseur en implémentant toutes les méthodes et en s’inscrivant correctement.</span><span class="sxs-lookup"><span data-stu-id="27b29-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



