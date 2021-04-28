---
description: 64 bits uniquement
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: 64 bits uniquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088807"
---
# <a name="64-bit-only"></a><span data-ttu-id="98084-103">64 bits uniquement</span><span class="sxs-lookup"><span data-stu-id="98084-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="98084-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="98084-104">Affected Platforms</span></span>

<span data-ttu-id="98084-105">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98084-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="98084-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="98084-106">Feature Impact</span></span>

 <span data-ttu-id="98084-107">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="98084-107">**Severity** - Low</span></span>  
<span data-ttu-id="98084-108">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="98084-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="98084-109">Description</span><span class="sxs-lookup"><span data-stu-id="98084-109">Description</span></span>

<span data-ttu-id="98084-110">Windows Server 2008 R2 est fourni avec une référence SKU 64 bits uniquement. aucune référence SKU 32 bits n’est disponible pour la version serveur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="98084-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="98084-111">Toutefois, une référence SKU 32 bits continue d’être disponible pour le client Windows 7.</span><span class="sxs-lookup"><span data-stu-id="98084-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="98084-112">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="98084-112">Manifestation of Impact</span></span>

<span data-ttu-id="98084-113">Cela aura un impact sur trois domaines :</span><span class="sxs-lookup"><span data-stu-id="98084-113">This will impact three areas:</span></span>

-   <span data-ttu-id="98084-114">pilotes 32 bits</span><span class="sxs-lookup"><span data-stu-id="98084-114">32-bit drivers</span></span>
-   <span data-ttu-id="98084-115">plug-ins 32 bits</span><span class="sxs-lookup"><span data-stu-id="98084-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="98084-116">exécutables 16 bits</span><span class="sxs-lookup"><span data-stu-id="98084-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="98084-117">Solution pour les pilotes 32 bits</span><span class="sxs-lookup"><span data-stu-id="98084-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="98084-118">Recompilez les pilotes 32 bits comme des pilotes signés 64 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="98084-119">Solution pour les plug-ins 32 bits</span><span class="sxs-lookup"><span data-stu-id="98084-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="98084-120">WoW64, un émulateur x86, permet aux applications basées sur Windows 32 bits de s’exécuter de façon transparente sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="98084-121">WoW64 est désormais une fonctionnalité facultative que vous devez installer si nécessaire pour exécuter du code 32 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="98084-122">Le système isole les applications 32 bits des applications 64 bits, ce qui comprend la prévention des collisions de fichiers et de registres.</span><span class="sxs-lookup"><span data-stu-id="98084-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="98084-123">Les applications console, GUI et de service sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="98084-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="98084-124">Le système fournit une interopérabilité à travers la limite 32/64 pour des scénarios tels que couper et coller et COM.</span><span class="sxs-lookup"><span data-stu-id="98084-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="98084-125">Toutefois, les processus 32 bits ne peuvent pas charger les dll 64 bits et les processus 64 bits ne peuvent pas charger de dll 32 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="98084-126">Nous le voyons généralement dans les plug-ins Shell écrits pour l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="98084-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="98084-127">Une application 32 bits peut détecter si elle s’exécute sous WOW64 en appelant la fonction IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="98084-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="98084-128">L’application peut obtenir des informations supplémentaires sur le processeur à l’aide de la fonction GetNativeSystemInfo</span><span class="sxs-lookup"><span data-stu-id="98084-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="98084-129">Notez que Windows 64 bits ne prend pas en charge l’exécution d’applications Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="98084-130">La raison principale est que les handles ont 32 bits significatifs sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="98084-131">Par conséquent, les handles ne peuvent pas être tronqués et passés à des applications 16 bits sans perte de données.</span><span class="sxs-lookup"><span data-stu-id="98084-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="98084-132">Les tentatives de lancement d’applications 16 bits échouent avec l’erreur suivante : erreur \_ \_ format exe incorrect \_ .</span><span class="sxs-lookup"><span data-stu-id="98084-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="98084-133">Solution pour les exécutables 16 bits</span><span class="sxs-lookup"><span data-stu-id="98084-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="98084-134">Windows 64 bits reconnaît un nombre limité de programmes d’installation 16 bits spécifiques et remplace une version 32 bits par un port.</span><span class="sxs-lookup"><span data-stu-id="98084-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="98084-135">La liste des substitutions est stockée dans le Registre sous la clé suivante : HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 il existe une prise en charge intégrée de plusieurs moteurs d’installation, y compris les programmes d’installation InstallShield 5. x.</span><span class="sxs-lookup"><span data-stu-id="98084-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="98084-136">Notez que l’Windows Installer 64 bits peut installer en toute transparence des applications MSI 32 bits sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="98084-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="98084-137">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="98084-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="98084-138">Exécution d’applications 32 bits</span><span class="sxs-lookup"><span data-stu-id="98084-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="98084-139">Performances et consommation de mémoire</span><span class="sxs-lookup"><span data-stu-id="98084-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="98084-140">Détails de l’implémentation WOW64</span><span class="sxs-lookup"><span data-stu-id="98084-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="98084-141">Redirecteur du Registre</span><span class="sxs-lookup"><span data-stu-id="98084-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="98084-142">Redirecteur de système de fichiers</span><span class="sxs-lookup"><span data-stu-id="98084-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="98084-143">Gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="98084-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="98084-144">Affinité du processeur</span><span class="sxs-lookup"><span data-stu-id="98084-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="98084-145">Communication entre processus</span><span class="sxs-lookup"><span data-stu-id="98084-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="98084-146">Installation d’applications sur des systèmes 64 bits</span><span class="sxs-lookup"><span data-stu-id="98084-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="98084-147">Débogage de WOW64</span><span class="sxs-lookup"><span data-stu-id="98084-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="98084-148">**IsWow64Process fonction)**</span><span class="sxs-lookup"><span data-stu-id="98084-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="98084-149">**GetNativeSystemInfo fonction)**</span><span class="sxs-lookup"><span data-stu-id="98084-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
