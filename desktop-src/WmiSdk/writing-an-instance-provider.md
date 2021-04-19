---
description: Un fournisseur d’instances fournit des instances d’une ou de plusieurs classes données.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Écriture d’un fournisseur d’instances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536696"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="06faf-103">Écriture d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="06faf-103">Writing an Instance Provider</span></span>

<span data-ttu-id="06faf-104">Un fournisseur d’instances fournit des instances d’une ou de plusieurs classes données.</span><span class="sxs-lookup"><span data-stu-id="06faf-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="06faf-105">Par exemple, un fournisseur d’instances peut fournir des informations sur un processeur ou un autre type de matériel.</span><span class="sxs-lookup"><span data-stu-id="06faf-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="06faf-106">Étant donné que les objets gérés par un fournisseur d’instances ont tendance à changer régulièrement, tous les fournisseurs d’instances sont considérés comme des fournisseurs d’extraction ; autrement dit, un fournisseur qui récupère dynamiquement les informations relatives à un objet managé chaque fois que WMI effectue une demande d’informations.</span><span class="sxs-lookup"><span data-stu-id="06faf-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="06faf-107">Le nom provient de l’idée que WMI « extrait » les informations du fournisseur pour le compte de la demande d’un client.</span><span class="sxs-lookup"><span data-stu-id="06faf-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="06faf-108">À l’aide de la technologie pull, un fournisseur d’instances peut prendre en charge la récupération, l’énumération, la modification, la suppression et le traitement des requêtes d’une instance spécifique.</span><span class="sxs-lookup"><span data-stu-id="06faf-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="06faf-109">Les fournisseurs de haute performance peuvent augmenter l’efficacité d’un fournisseur d’instances ou accéder par programmation aux données qui apparaissent dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="06faf-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="06faf-110">Pour plus d’informations, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="06faf-111">La procédure suivante décrit comment écrire un fournisseur d’instances.</span><span class="sxs-lookup"><span data-stu-id="06faf-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="06faf-112">**Pour écrire un fournisseur d’instances**</span><span class="sxs-lookup"><span data-stu-id="06faf-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="06faf-113">[Inscrivez votre fournisseur auprès de WMI](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="06faf-114">Les fournisseurs d’instances s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="06faf-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="06faf-115">[Initialisez votre fournisseur](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="06faf-116">WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="06faf-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="06faf-117">Il s’agit d’une tâche commune à tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="06faf-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="06faf-118">Les fournisseurs d’instances sont fortement encouragés à utiliser le modèle de multithreading « both ».</span><span class="sxs-lookup"><span data-stu-id="06faf-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="06faf-119">[Implémentez l’interface IWbemServices pour votre fournisseur](implementing-the-primary-interface-for-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="06faf-120">L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) est l’interface principale d’un fournisseur d’instances.</span><span class="sxs-lookup"><span data-stu-id="06faf-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="06faf-121">Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="06faf-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="06faf-122">Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="06faf-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="06faf-123">Pour plus d’informations, consultez [effectuer des appels à WMI](making-calls-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="06faf-124">Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client.</span><span class="sxs-lookup"><span data-stu-id="06faf-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="06faf-125">Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="06faf-126">Si nécessaire, [implémentez l’interface hautes performances](improving-the-efficiency-of-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="06faf-127">L’interface hautes performances augmente la vitesse à laquelle le fournisseur peut réagir aux demandes de WMI.</span><span class="sxs-lookup"><span data-stu-id="06faf-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="06faf-128">Si nécessaire, [implémentez la prise en charge des mises à jour d’instance partielle](supporting-partial-instance-operations.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="06faf-129">Comme son nom l’indique, une mise à jour de l’instance partielle est une technique qui permet de mettre à jour uniquement une partie d’une instance.</span><span class="sxs-lookup"><span data-stu-id="06faf-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="06faf-130">Pour plus d’informations sur l’appel d’une instance partielle à partir d’un client, consultez [mise à jour d’une partie d’une instance](updating-part-of-an-instance.md) et [extraction d’une partie d’une instance WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="06faf-131">Remplacez le fournisseur préexistant par votre nouveau code.</span><span class="sxs-lookup"><span data-stu-id="06faf-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="06faf-132">Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier.</span><span class="sxs-lookup"><span data-stu-id="06faf-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="06faf-133">Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06faf-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



