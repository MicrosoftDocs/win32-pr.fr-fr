---
description: Étant donné que WMI charge un fournisseur de haute performance dans le processus vers WMI ou une application cliente, vous devez concevoir votre fournisseur hautes performances en tant que serveur in-process.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implémentation de l’interface High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538916"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="3621c-103">Implémentation de l’interface High-Performance</span><span class="sxs-lookup"><span data-stu-id="3621c-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="3621c-104">Étant donné que WMI charge un fournisseur de haute performance dans le processus vers WMI ou une application cliente, vous devez concevoir votre fournisseur hautes performances en tant que serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="3621c-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="3621c-105">En outre, vous devez implémenter les méthodes de fournisseur de haute performance dans les interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) et [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .</span><span class="sxs-lookup"><span data-stu-id="3621c-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="3621c-106">Vous devez implémenter un fournisseur de haute performance en tant que serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="3621c-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="3621c-107">L’une des fonctionnalités que vous devez prendre en compte lors de l’implémentation de la sécurité d’un serveur in-process est la manière dont le fournisseur identifie son propre emplacement.</span><span class="sxs-lookup"><span data-stu-id="3621c-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="3621c-108">Lorsqu’il est chargé dans le processus de WMI, WMI instancie le fournisseur à l’aide d’un CLSID.</span><span class="sxs-lookup"><span data-stu-id="3621c-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="3621c-109">Lorsqu’il est chargé en cours de traitement dans une application cliente, l’application cliente instancie le fournisseur avec la propriété **ClientLoadableCLSID** .</span><span class="sxs-lookup"><span data-stu-id="3621c-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="3621c-110">En attribuant des valeurs différentes à un CLSID et à **ClientLoadableCLSID**, vous autorisez le fournisseur à déterminer s’il est chargé dans le processus vers WMI ou vers une application cliente.</span><span class="sxs-lookup"><span data-stu-id="3621c-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="3621c-111">Si elle se trouve dans un processus WMI, le fournisseur doit effectuer l’emprunt d’identité du client nécessaire à l’aide de **ClientLoadableCLSID**.</span><span class="sxs-lookup"><span data-stu-id="3621c-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="3621c-112">Si elle se trouve dans un processus client, le fournisseur hérite du jeton d’accès du thread sur lequel elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="3621c-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="3621c-113">Pour plus d’informations sur l’implémentation d’un serveur in-process, consultez la [section com](https://msdn.microsoft.com/library/aa139695.aspx) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="3621c-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="3621c-114">En tant que serveur in-process, un fournisseur de haute performance utilise un objet actualisateur pour conserver les données à jour pour le client distant.</span><span class="sxs-lookup"><span data-stu-id="3621c-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="3621c-115">Le tableau suivant répertorie les méthodes que vous devez implémenter pour un fournisseur à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="3621c-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="3621c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="3621c-116">Method</span></span>                                                                                              | <span data-ttu-id="3621c-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="3621c-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="3621c-118">**IWbemHiPerfProvider :: QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="3621c-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="3621c-119">Requêtes</span><span class="sxs-lookup"><span data-stu-id="3621c-119">Queries</span></span>                                           |
| [<span data-ttu-id="3621c-120">**IWbemHiPerfProvider :: GetObjects**</span><span class="sxs-lookup"><span data-stu-id="3621c-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="3621c-121">Récupération d’objets</span><span class="sxs-lookup"><span data-stu-id="3621c-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="3621c-122">**IWbemHiPerfProvider :: CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="3621c-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="3621c-123">Crée un actualisateur</span><span class="sxs-lookup"><span data-stu-id="3621c-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="3621c-124">**IWbemHiPerfProvider :: CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="3621c-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="3621c-125">Crée un objet d’instance actualisable</span><span class="sxs-lookup"><span data-stu-id="3621c-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="3621c-126">**IWbemHiPerfProvider :: CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="3621c-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="3621c-127">Crée un énumérateur actualisable</span><span class="sxs-lookup"><span data-stu-id="3621c-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="3621c-128">**IWbemHiPerfProvider :: StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="3621c-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="3621c-129">Arrête l’actualisation d’un objet énumérateur ou d’instance</span><span class="sxs-lookup"><span data-stu-id="3621c-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="3621c-130">**IWbemRefresher :: Refresh**</span><span class="sxs-lookup"><span data-stu-id="3621c-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="3621c-131">Crée un actualisateur</span><span class="sxs-lookup"><span data-stu-id="3621c-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="3621c-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3621c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3621c-133">Création d’un fournisseur d’instances dans un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="3621c-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



