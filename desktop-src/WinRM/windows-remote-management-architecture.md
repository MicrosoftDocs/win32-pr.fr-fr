---
title: Architecture Windows Remote Management
description: L’architecture Windows Remote Management se compose de composants sur les ordinateurs clients et serveurs.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729188"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="56efd-103">Architecture Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="56efd-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="56efd-104">L’architecture Windows Remote Management se compose de composants sur les ordinateurs clients et serveurs.</span><span class="sxs-lookup"><span data-stu-id="56efd-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="56efd-105">L’illustration suivante montre les composants sur les deux ordinateurs, la façon dont les composants interagissent avec d’autres composants et le protocole utilisé pour la communication entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="56efd-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![architecture WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="56efd-107">Client demandeur</span><span class="sxs-lookup"><span data-stu-id="56efd-107">Requesting Client</span></span>

<span data-ttu-id="56efd-108">Les composants WinRM suivants résident sur l’ordinateur qui exécute le script qui demande des données.</span><span class="sxs-lookup"><span data-stu-id="56efd-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="56efd-109">Application WinRM</span><span class="sxs-lookup"><span data-stu-id="56efd-109">WinRM application</span></span>

    <span data-ttu-id="56efd-110">Il s’agit du script ou de l’outil de ligne de commande **WinRM** qui utilise l’API de script WinRM pour effectuer des appels pour demander des données ou exécuter des méthodes.</span><span class="sxs-lookup"><span data-stu-id="56efd-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="56efd-111">Pour plus d’informations, consultez l' [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="56efd-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="56efd-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-112">WSMAuto.dll</span></span>

    <span data-ttu-id="56efd-113">Couche Automation qui fournit la prise en charge des scripts.</span><span class="sxs-lookup"><span data-stu-id="56efd-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="56efd-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-114">WsmCL.dll</span></span>

    <span data-ttu-id="56efd-115">Couche d’API C dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="56efd-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="56efd-116">API HTTP</span><span class="sxs-lookup"><span data-stu-id="56efd-116">HTTP API</span></span>

    <span data-ttu-id="56efd-117">WinRM requiert la prise en charge du transport HTTP et HTTPs.</span><span class="sxs-lookup"><span data-stu-id="56efd-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="56efd-118">Serveur de réponse</span><span class="sxs-lookup"><span data-stu-id="56efd-118">Responding Server</span></span>

<span data-ttu-id="56efd-119">Les composants WinRM suivants résident sur l’ordinateur qui répond.</span><span class="sxs-lookup"><span data-stu-id="56efd-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="56efd-120">API HTTP</span><span class="sxs-lookup"><span data-stu-id="56efd-120">HTTP API</span></span>

    <span data-ttu-id="56efd-121">WinRM requiert la prise en charge du transport HTTP et HTTPs.</span><span class="sxs-lookup"><span data-stu-id="56efd-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="56efd-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-122">WSMAuto.dll</span></span>

    <span data-ttu-id="56efd-123">Couche Automation qui fournit la prise en charge des scripts.</span><span class="sxs-lookup"><span data-stu-id="56efd-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="56efd-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-124">WsmCL.dll</span></span>

    <span data-ttu-id="56efd-125">Couche d’API C dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="56efd-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="56efd-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-126">WsmSvc.dll</span></span>

    <span data-ttu-id="56efd-127">Service d' [*écoute*](windows-remote-management-glossary.md) WinRM.</span><span class="sxs-lookup"><span data-stu-id="56efd-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="56efd-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-128">WsmProv.dll</span></span>

    <span data-ttu-id="56efd-129">Sous-système du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="56efd-129">Provider subsystem.</span></span>

-   <span data-ttu-id="56efd-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-130">WsmRes.dll</span></span>

    <span data-ttu-id="56efd-131">Fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="56efd-131">Resource file.</span></span>

-   <span data-ttu-id="56efd-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="56efd-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="56efd-133">[*Plug-in WMI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="56efd-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="56efd-134">Cela vous permet d’obtenir des données WMI via WinRM.</span><span class="sxs-lookup"><span data-stu-id="56efd-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="56efd-135">Pilote IPMI (Intelligent Platform Management Interface) et fournisseur IPMI WMI</span><span class="sxs-lookup"><span data-stu-id="56efd-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="56efd-136">Ces composants fournissent toutes les données matérielles demandées à l’aide des classes IPMI.</span><span class="sxs-lookup"><span data-stu-id="56efd-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="56efd-137">Pour plus d’informations, consultez [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="56efd-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="56efd-138">Le matériel BMC doit avoir été détecté par le SMBIOS ou l’appareil créé manuellement par le chargement du pilote.</span><span class="sxs-lookup"><span data-stu-id="56efd-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="56efd-139">Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="56efd-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56efd-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56efd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56efd-141">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="56efd-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 