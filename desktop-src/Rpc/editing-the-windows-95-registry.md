---
title: Modification du registre de Windows 95
description: Vous pouvez utiliser REGEDIT pour modifier le Registre Windows 95 afin de désigner un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840657"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="0f39e-103">Modification du registre de Windows 95</span><span class="sxs-lookup"><span data-stu-id="0f39e-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="0f39e-104">Vous pouvez utiliser REGEDIT pour modifier le Registre Windows 95 afin de désigner un NSP.</span><span class="sxs-lookup"><span data-stu-id="0f39e-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="0f39e-105">**Pour désigner un fournisseur de services de noms Microsoft Locator pour Windows 95**</span><span class="sxs-lookup"><span data-stu-id="0f39e-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="0f39e-106">Sélectionnez</span><span class="sxs-lookup"><span data-stu-id="0f39e-106">Select</span></span>

    <span data-ttu-id="0f39e-107">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="0f39e-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="0f39e-108">Créer une nouvelle clé appelée</span><span class="sxs-lookup"><span data-stu-id="0f39e-108">Create a new key called</span></span>

    <span data-ttu-id="0f39e-109">**NameService**</span><span class="sxs-lookup"><span data-stu-id="0f39e-109">**NameService**</span></span>

3.  <span data-ttu-id="0f39e-110">Une fois la clé **NameService** sélectionnée, créez les noms de **StringValue** et modifiez-les pour qu’ils contiennent les données, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0f39e-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="0f39e-111">Nom</span><span class="sxs-lookup"><span data-stu-id="0f39e-111">Name</span></span>                     | <span data-ttu-id="0f39e-112">Données</span><span class="sxs-lookup"><span data-stu-id="0f39e-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="0f39e-113">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="0f39e-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="0f39e-114">3</span><span class="sxs-lookup"><span data-stu-id="0f39e-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="0f39e-115">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="0f39e-115">**Protocol**</span></span>             | <span data-ttu-id="0f39e-116">ncacn \_ NP</span><span class="sxs-lookup"><span data-stu-id="0f39e-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="0f39e-117">**Point de terminaison**</span><span class="sxs-lookup"><span data-stu-id="0f39e-117">**Endpoint**</span></span>             | <span data-ttu-id="0f39e-118">\\Localisateur de canal \\</span><span class="sxs-lookup"><span data-stu-id="0f39e-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="0f39e-119">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="0f39e-119">**NetworkAddress**</span></span>       | <span data-ttu-id="0f39e-120">MyServer (où MyServer est le nom de l’ordinateur Windows NT)</span><span class="sxs-lookup"><span data-stu-id="0f39e-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="0f39e-121">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="0f39e-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="0f39e-122">MyServer</span><span class="sxs-lookup"><span data-stu-id="0f39e-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="0f39e-123">Vous pouvez utiliser REGEDIT pour modifier le Registre Windows 95 afin de désigner un NSP CDS CDS.</span><span class="sxs-lookup"><span data-stu-id="0f39e-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="0f39e-124">**Pour désigner un fournisseur de services de noms de CD DCE pour Windows 95**</span><span class="sxs-lookup"><span data-stu-id="0f39e-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="0f39e-125">Sélectionnez</span><span class="sxs-lookup"><span data-stu-id="0f39e-125">Select</span></span>

    <span data-ttu-id="0f39e-126">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="0f39e-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="0f39e-127">Créer une nouvelle clé appelée</span><span class="sxs-lookup"><span data-stu-id="0f39e-127">Create a new key called</span></span>

    <span data-ttu-id="0f39e-128">**NameService**</span><span class="sxs-lookup"><span data-stu-id="0f39e-128">**NameService**</span></span>

3.  <span data-ttu-id="0f39e-129">Une fois la clé **NameService** sélectionnée, créez les noms de **StringValue** et modifiez-les pour qu’ils contiennent les données, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0f39e-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="0f39e-130">Nom</span><span class="sxs-lookup"><span data-stu-id="0f39e-130">Name</span></span>                     | <span data-ttu-id="0f39e-131">Données</span><span class="sxs-lookup"><span data-stu-id="0f39e-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="0f39e-132">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="0f39e-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="0f39e-133">3</span><span class="sxs-lookup"><span data-stu-id="0f39e-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="0f39e-134">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="0f39e-134">**Protocol**</span></span>             | <span data-ttu-id="0f39e-135">\_TCP IP \_ ncacn</span><span class="sxs-lookup"><span data-stu-id="0f39e-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="0f39e-136">**Point de terminaison**</span><span class="sxs-lookup"><span data-stu-id="0f39e-136">**Endpoint**</span></span>             | <span data-ttu-id="0f39e-137">"" (chaîne vide)</span><span class="sxs-lookup"><span data-stu-id="0f39e-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="0f39e-138">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="0f39e-138">**NetworkAddress**</span></span>       | <span data-ttu-id="0f39e-139">monserveur (nom de l’ordinateur hôte exécutant NSID)</span><span class="sxs-lookup"><span data-stu-id="0f39e-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="0f39e-140">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="0f39e-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="0f39e-141">monserveur (nom de l’ordinateur hôte exécutant NSID)</span><span class="sxs-lookup"><span data-stu-id="0f39e-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="0f39e-142">Vous devez avoir le produit DCE service d’annuaire de cellules/service d’annuaires de cellules Digital Equipment Corporation pour configurer les CDS DCE en tant que fournisseur de services de noms.</span><span class="sxs-lookup"><span data-stu-id="0f39e-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="0f39e-143">Consultez la documentation fournie par Digital Equipment Corporation pour plus d’informations sur les CDS DCE.</span><span class="sxs-lookup"><span data-stu-id="0f39e-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





