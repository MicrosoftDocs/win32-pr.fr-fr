---
title: Développement d’applications Windows RPC
description: Lorsque vous installez le kit de développement logiciel (SDK) de la plateforme, l’environnement de développement RPC, les bibliothèques d’exécution et les outils suivants sont installés automatiquement
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031747"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="732fd-103">Développement d’applications Windows RPC</span><span class="sxs-lookup"><span data-stu-id="732fd-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="732fd-104">Lorsque vous installez le kit de développement logiciel (SDK) de la plateforme, l’environnement de développement RPC suivant, les bibliothèques Runtime et les outils sont automatiquement installés :</span><span class="sxs-lookup"><span data-stu-id="732fd-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="732fd-105">En-tête du langage C/C++ (. H)</span><span class="sxs-lookup"><span data-stu-id="732fd-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="732fd-106">Fichiers de bibliothèque d’importation RPC (. lib)</span><span class="sxs-lookup"><span data-stu-id="732fd-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="732fd-107">Exemples de programmes</span><span class="sxs-lookup"><span data-stu-id="732fd-107">Sample programs</span></span>
-   <span data-ttu-id="732fd-108">Fichiers d’aide de référence RPC</span><span class="sxs-lookup"><span data-stu-id="732fd-108">RPC reference Help files</span></span>
-   <span data-ttu-id="732fd-109">Utilitaire **uuidgen**</span><span class="sxs-lookup"><span data-stu-id="732fd-109">The **uuidgen** utility</span></span>

<span data-ttu-id="732fd-110">Lorsque vous installez Windows, les éléments suivants sont installés :</span><span class="sxs-lookup"><span data-stu-id="732fd-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="732fd-111">Dll Runtime RPC</span><span class="sxs-lookup"><span data-stu-id="732fd-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="732fd-112">Microsoft Locator (non pris en charge sur Windows Vista et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="732fd-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="732fd-113">Services de mappage de point de terminaison RPC</span><span class="sxs-lookup"><span data-stu-id="732fd-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="732fd-114">Bibliothèques d’importation RPC suivantes.</span><span class="sxs-lookup"><span data-stu-id="732fd-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="732fd-115">Importer la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="732fd-115">Import library</span></span> | <span data-ttu-id="732fd-116">Description</span><span class="sxs-lookup"><span data-stu-id="732fd-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="732fd-117">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="732fd-117">Rpcns4.lib</span></span>     | <span data-ttu-id="732fd-118">Fonctions Name-Service</span><span class="sxs-lookup"><span data-stu-id="732fd-118">Name-service functions</span></span>     |
| <span data-ttu-id="732fd-119">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="732fd-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="732fd-120">Fonctions runtime Windows</span><span class="sxs-lookup"><span data-stu-id="732fd-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="732fd-121">Rpcns4. lib est obsolète et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="732fd-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="732fd-122">Les bibliothèques RPC suivantes sont incluses pour la prise en charge de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="732fd-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="732fd-123">Bibliothèque de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="732fd-123">Dynamic-link library</span></span> | <span data-ttu-id="732fd-124">Description</span><span class="sxs-lookup"><span data-stu-id="732fd-124">Description</span></span>                 | <span data-ttu-id="732fd-125">Plate-forme</span><span class="sxs-lookup"><span data-stu-id="732fd-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="732fd-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="732fd-127">Transport du canal nommé du client</span><span class="sxs-lookup"><span data-stu-id="732fd-127">Client named-pipe transport</span></span> | <span data-ttu-id="732fd-128">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-129">Rpclts1.dll</span></span>          | <span data-ttu-id="732fd-130">Transport de canaux nommés du serveur</span><span class="sxs-lookup"><span data-stu-id="732fd-130">Server named-pipe transport</span></span> | <span data-ttu-id="732fd-131">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="732fd-133">Transport TCP/IP du client</span><span class="sxs-lookup"><span data-stu-id="732fd-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="732fd-134">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-135">Rpclts3.dll</span></span>          | <span data-ttu-id="732fd-136">Transport TCP/IP du serveur</span><span class="sxs-lookup"><span data-stu-id="732fd-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="732fd-137">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="732fd-139">Transport NetBIOS du client</span><span class="sxs-lookup"><span data-stu-id="732fd-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="732fd-140">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-141">Rpclts5.dll</span></span>          | <span data-ttu-id="732fd-142">Transport NetBIOS du serveur</span><span class="sxs-lookup"><span data-stu-id="732fd-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="732fd-143">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="732fd-145">Transport SPX client</span><span class="sxs-lookup"><span data-stu-id="732fd-145">Client SPX transport</span></span>        | <span data-ttu-id="732fd-146">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-147">Rpclts6.dll</span></span>          | <span data-ttu-id="732fd-148">Transport du serveur SPX</span><span class="sxs-lookup"><span data-stu-id="732fd-148">Server SPX transport</span></span>        | <span data-ttu-id="732fd-149">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="732fd-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="732fd-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="732fd-151">Transport IPX du client</span><span class="sxs-lookup"><span data-stu-id="732fd-151">Client IPX transport</span></span>        | <span data-ttu-id="732fd-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="732fd-152">Windows NT</span></span>                         |
| <span data-ttu-id="732fd-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="732fd-154">Transport IPX du serveur</span><span class="sxs-lookup"><span data-stu-id="732fd-154">Server IPX transport</span></span>        | <span data-ttu-id="732fd-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="732fd-155">Windows NT</span></span>                         |
| <span data-ttu-id="732fd-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="732fd-157">Transport UDP du client</span><span class="sxs-lookup"><span data-stu-id="732fd-157">Client UDP transport</span></span>        | <span data-ttu-id="732fd-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="732fd-158">Windows NT</span></span>                         |
| <span data-ttu-id="732fd-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="732fd-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="732fd-160">Transport UDP du serveur</span><span class="sxs-lookup"><span data-stu-id="732fd-160">Server UDP transport</span></span>        | <span data-ttu-id="732fd-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="732fd-161">Windows NT</span></span>                         |



 

<span data-ttu-id="732fd-162">Vous aurez également besoin du compilateur Microsoft Interface Definition Language (MIDL).</span><span class="sxs-lookup"><span data-stu-id="732fd-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="732fd-163">Pour plus d’informations, consultez [utilisation du compilateur MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).</span><span class="sxs-lookup"><span data-stu-id="732fd-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 