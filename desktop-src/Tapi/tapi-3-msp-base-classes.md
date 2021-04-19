---
description: Ce document décrit la conception et l’utilisation des classes de base MSP. L’utilisation de ces classes n’est pas obligatoire, mais la plupart des développeurs trouveront qu’ils simplifieront la tâche de création d’un MSP basé sur DirectShow pour TAPI 3S New MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classes de base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535570"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="6f18c-104">Classes de base TAPI 3 MSP</span><span class="sxs-lookup"><span data-stu-id="6f18c-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="6f18c-105">Ce document décrit la conception et l’utilisation des classes de base MSP.</span><span class="sxs-lookup"><span data-stu-id="6f18c-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="6f18c-106">L’utilisation de ces classes n’est pas obligatoire, mais la plupart des développeurs trouvent qu’ils simplifient la création d’un MSP basé sur DirectShow pour le nouveau MSPI de l’interface TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="6f18c-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="6f18c-107">Le code source pour les classes de base MSP se trouve dans le répertoire Samples du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="6f18c-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="6f18c-108">Il est supposé que vous êtes familiarisé avec COM, ATL, DirectShow et C++.</span><span class="sxs-lookup"><span data-stu-id="6f18c-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="6f18c-109">Le lecteur doit également connaître les informations générales dans [à propos du fournisseur de services multimédia (MSP)](about-the-media-service-provider-msp-.md) et de l' [interface MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-.md).</span><span class="sxs-lookup"><span data-stu-id="6f18c-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="6f18c-110">ATL 2,1 est requis pour Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6f18c-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="6f18c-111">À compter de Windows XP, ATL 2,1 et 3,0 se compilent à la fois.</span><span class="sxs-lookup"><span data-stu-id="6f18c-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="6f18c-112">Bibliothèques de classes de base MSP (disponibles dans le kit de développement logiciel (SDK)) :</span><span class="sxs-lookup"><span data-stu-id="6f18c-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="6f18c-113">Mspbase. lib</span><span class="sxs-lookup"><span data-stu-id="6f18c-113">Mspbase.lib</span></span>
-   <span data-ttu-id="6f18c-114">Mspid. lib</span><span class="sxs-lookup"><span data-stu-id="6f18c-114">Mspid.lib</span></span>
-   <span data-ttu-id="6f18c-115">Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="6f18c-115">Strmbase.lib</span></span>
-   <span data-ttu-id="6f18c-116">Tmuid. lib</span><span class="sxs-lookup"><span data-stu-id="6f18c-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="6f18c-117">Les liaisons dynamiques et non statiques doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="6f18c-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="6f18c-118">Fichiers d’en-tête de classe de base MSP (disponibles dans le kit de développement logiciel) :</span><span class="sxs-lookup"><span data-stu-id="6f18c-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="6f18c-119">Mspaddr. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-119">Mspaddr.h</span></span>
-   <span data-ttu-id="6f18c-120">Mspbase. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-120">Mspbase.h</span></span>
-   <span data-ttu-id="6f18c-121">Mspcall. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-121">Mspcall.h</span></span>
-   <span data-ttu-id="6f18c-122">Msplog. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-122">Msplog.h</span></span>
-   <span data-ttu-id="6f18c-123">Mspstrm. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-123">Mspstrm.h</span></span>
-   <span data-ttu-id="6f18c-124">Mspterm. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-124">Mspterm.h</span></span>
-   <span data-ttu-id="6f18c-125">Mspthrd. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-125">Mspthrd.h</span></span>
-   <span data-ttu-id="6f18c-126">Msptmac. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-126">Msptmac.h</span></span>
-   <span data-ttu-id="6f18c-127">Msptmvc. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-127">Msptmvc.h</span></span>
-   <span data-ttu-id="6f18c-128">Msptrmvc. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="6f18c-129">Msptrmac. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-129">Msptrmac.h</span></span>
-   <span data-ttu-id="6f18c-130">Msptrmar. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-130">Msptrmar.h</span></span>
-   <span data-ttu-id="6f18c-131">Msputils. h</span><span class="sxs-lookup"><span data-stu-id="6f18c-131">Msputils.h</span></span>

<span data-ttu-id="6f18c-132">Fichiers sources de la classe de base MSP (disponibles dans les exemples du kit de développement logiciel) :</span><span class="sxs-lookup"><span data-stu-id="6f18c-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="6f18c-133">Mspaddr. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="6f18c-134">Mspcall. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="6f18c-135">Msplog. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-135">Msplog.cpp</span></span>
-   <span data-ttu-id="6f18c-136">Mspstrm. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="6f18c-137">Mspterm. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="6f18c-138">Mspthrd. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="6f18c-139">Msptrmac. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="6f18c-140">Msptrmar. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="6f18c-141">Msptrmvc. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="6f18c-142">Msputils. cpp</span><span class="sxs-lookup"><span data-stu-id="6f18c-142">Msputils.cpp</span></span>

 

 



