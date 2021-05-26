---
title: Service de transfert intelligent en arrière-plan (BITS)
description: Le service de transfert intelligent en arrière-plan (BITS) transfère des fichiers (téléchargement ou chargement) entre un client et un serveur et fournit des informations d’avancement liées aux transferts.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan, page de démarrage
- BITS (voir Service de transfert intelligent en arrière-plan)
- Téléchargement des fichiers BITS
- BITS de transfert de fichiers en arrière-plan
- Téléchargement des fichiers BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 9483e297e8b48ad6466846c7eceb8d53b57d3278
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424209"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="860c7-109">Service de transfert intelligent en arrière-plan (BITS)</span><span class="sxs-lookup"><span data-stu-id="860c7-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="860c7-110">Objectif</span><span class="sxs-lookup"><span data-stu-id="860c7-110">Purpose</span></span>

<span data-ttu-id="860c7-111">Service de transfert intelligent en arrière-plan (BITS) est utilisé par les programmeurs et les administrateurs système pour télécharger des fichiers depuis ou vers des serveurs Web HTTP et des partages de fichiers SMB.</span><span class="sxs-lookup"><span data-stu-id="860c7-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="860c7-112">Le service BITS prend en compte le coût du transfert, ainsi que l’utilisation du réseau afin que le travail de premier plan de l’utilisateur ait le moins d’impact possible.</span><span class="sxs-lookup"><span data-stu-id="860c7-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="860c7-113">BITS gère également les interuptions réseau, en suspendant et en reprenant automatiquement les transferts, même après un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="860c7-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="860c7-114">Le service BITS comprend des applets de commande PowerShell pour la création et la gestion des transferts, ainsi que l’utilitaire de ligne de commande BitsAdmin.</span><span class="sxs-lookup"><span data-stu-id="860c7-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="860c7-115">Le service BITS peut être utilisé par Windows pour télécharger les mises à jour sur votre système local.</span><span class="sxs-lookup"><span data-stu-id="860c7-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="860c7-116">Si vous êtes un utilisateur final qui recherche des moyens de résoudre les problèmes liés à l’installation de BITS, consultez [résoudre les problèmes de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span><span class="sxs-lookup"><span data-stu-id="860c7-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="860c7-117">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="860c7-117">Where applicable</span></span>

<span data-ttu-id="860c7-118">Utilisez le service BITS pour les applications qui doivent :</span><span class="sxs-lookup"><span data-stu-id="860c7-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="860c7-119">Télécharger à partir de ou télécharger des fichiers sur un serveur Web HTTP ou REST ou un serveur de fichiers SMB.</span><span class="sxs-lookup"><span data-stu-id="860c7-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="860c7-120">Reprendre automatiquement les transferts de fichiers après la déconnexion du réseau et le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="860c7-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="860c7-121">Préserver la réactivité des autres applications réseau.</span><span class="sxs-lookup"><span data-stu-id="860c7-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="860c7-122">Gardez à l’esprit le coût du réseau, par exemple, les réseaux itinérants</span><span class="sxs-lookup"><span data-stu-id="860c7-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="860c7-123">Utiliser éventuellement [BranchCache](/windows-server/networking/branchcache/branchcache) pour optimiser le trafic du réseau étendu (WAN)</span><span class="sxs-lookup"><span data-stu-id="860c7-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="860c7-124">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="860c7-124">Developer audience</span></span>

<span data-ttu-id="860c7-125">BITS est une interface COM conçue pour les développeurs C et C++ qui peut également être utilisée par les développeurs .NET.</span><span class="sxs-lookup"><span data-stu-id="860c7-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="860c7-126">Les développeurs UWP doivent utiliser l’API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) et non l’API bits.</span><span class="sxs-lookup"><span data-stu-id="860c7-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="860c7-127">Versions de BITS</span><span class="sxs-lookup"><span data-stu-id="860c7-127">BITS versions</span></span>

<span data-ttu-id="860c7-128">Pour obtenir l’historique des versions et des informations sur les systèmes d’exploitation antérieurs, consultez [Nouveautés](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="860c7-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="860c7-129">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="860c7-129">In this section</span></span>



| <span data-ttu-id="860c7-130">Rubrique</span><span class="sxs-lookup"><span data-stu-id="860c7-130">Topic</span></span>                                                           | <span data-ttu-id="860c7-131">Description</span><span class="sxs-lookup"><span data-stu-id="860c7-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="860c7-132">À propos du service BITS</span><span class="sxs-lookup"><span data-stu-id="860c7-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="860c7-133">Informations générales sur le service BITS.</span><span class="sxs-lookup"><span data-stu-id="860c7-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="860c7-134">Utilisation de BITS</span><span class="sxs-lookup"><span data-stu-id="860c7-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="860c7-135">Guide de procédures pour le développement de clients BITS qui transfèrent des fichiers entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="860c7-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="860c7-136">Informations de référence sur BITS</span><span class="sxs-lookup"><span data-stu-id="860c7-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="860c7-137">Informations de référence pour les interfaces de programmation BITS.</span><span class="sxs-lookup"><span data-stu-id="860c7-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="860c7-138">Contient également des informations sur les exemples, les outils, les paramètres de serveur pour les travaux de chargement et le protocole de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="860c7-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="860c7-139">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="860c7-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="860c7-140">Informations à prendre en compte lors de la conception d’une application qui utilise BITS.</span><span class="sxs-lookup"><span data-stu-id="860c7-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="860c7-141">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="860c7-141">Additional resources</span></span>

<span data-ttu-id="860c7-142">Vous trouverez ci-dessous des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="860c7-142">The following are additional resources.</span></span>


|    <span data-ttu-id="860c7-143">Ressource</span><span class="sxs-lookup"><span data-stu-id="860c7-143">Resource</span></span>         |    <span data-ttu-id="860c7-144">Description</span><span class="sxs-lookup"><span data-stu-id="860c7-144">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="860c7-145">DLL de référence .NET</span><span class="sxs-lookup"><span data-stu-id="860c7-145">.NET Reference DLL</span></span>   | <span data-ttu-id="860c7-146">Pour plus d’informations sur l’utilisation de BITS à partir de .NET à l’aide de dll de référence, consultez [appel de bits à partir de .net avec des dll de référence](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="860c7-146">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="860c7-147">Wrapper .NET</span><span class="sxs-lookup"><span data-stu-id="860c7-147">.NET Wrapper</span></span>   | <span data-ttu-id="860c7-148">Pour les autres wrappers .NET pour BITS, vous pouvez rechercher [NuGet](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) pour les projets marqués avec la balise bits.</span><span class="sxs-lookup"><span data-stu-id="860c7-148">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

