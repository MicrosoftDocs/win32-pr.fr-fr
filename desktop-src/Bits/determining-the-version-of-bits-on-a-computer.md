---
title: Détermination de la version de BITS sur un ordinateur
description: Pour déterminer la version de BITS sur l’ordinateur client, vérifiez la version de QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671441"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="6becc-103">Détermination de la version de BITS sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="6becc-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="6becc-104">Pour déterminer la version de BITS sur l’ordinateur client, vérifiez la version de QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="6becc-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="6becc-105">Pour rechercher le numéro de version de la DLL :</span><span class="sxs-lookup"><span data-stu-id="6becc-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="6becc-106">Recherchez QMgr.dll dans% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="6becc-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="6becc-107">Cliquez avec le bouton droit sur QMgr.dll, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6becc-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="6becc-108">Cliquez sur l’onglet **version** .</span><span class="sxs-lookup"><span data-stu-id="6becc-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="6becc-109">Notez le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="6becc-109">Note the version number.</span></span>

<span data-ttu-id="6becc-110">Vous pouvez également utiliser le code PowerShell suivant pour déterminer la version du fichier. dll sur votre système :</span><span class="sxs-lookup"><span data-stu-id="6becc-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="6becc-111">Si la DLL existe également dans% windir% \\ system32 \\ bits, répétez les étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="6becc-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="6becc-112">BITS utilise la DLL avec le numéro de version le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="6becc-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="6becc-113">Le tableau suivant répertorie les versions de BITS et leurs numéros de version de fichier QMgr.dll correspondants.</span><span class="sxs-lookup"><span data-stu-id="6becc-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="6becc-114">Version de BITS</span><span class="sxs-lookup"><span data-stu-id="6becc-114">BITS version</span></span> | <span data-ttu-id="6becc-115">Numéro de version du fichier QMgr.dll</span><span class="sxs-lookup"><span data-stu-id="6becc-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="6becc-116">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="6becc-116">BITS 10.1</span></span>    | <span data-ttu-id="6becc-117">7.8. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-118">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="6becc-118">BITS 5.0</span></span>     | <span data-ttu-id="6becc-119">7.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-120">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="6becc-120">BITS 4.0</span></span>     | <span data-ttu-id="6becc-121">7.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-122">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="6becc-122">BITS 3.0</span></span>     | <span data-ttu-id="6becc-123">7.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-124">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="6becc-124">BITS 2.5</span></span>     | <span data-ttu-id="6becc-125">6.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-126">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="6becc-126">BITS 2.0</span></span>     | <span data-ttu-id="6becc-127">6.6. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-128">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="6becc-128">BITS 1.5</span></span>     | <span data-ttu-id="6becc-129">6,5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-130">BITS 1,2</span><span class="sxs-lookup"><span data-stu-id="6becc-130">BITS 1.2</span></span>     | <span data-ttu-id="6becc-131">6.2. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="6becc-132">BITS 1,0</span><span class="sxs-lookup"><span data-stu-id="6becc-132">BITS 1.0</span></span>     | <span data-ttu-id="6becc-133">6.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="6becc-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="6becc-134">Vous pouvez également utiliser les identificateurs de classe symbolique pour déterminer la version de BITS qui est inscrite sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6becc-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="6becc-135">Le tableau suivant répertorie les versions de BITS et leurs identificateurs de classe symbolique correspondants.</span><span class="sxs-lookup"><span data-stu-id="6becc-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="6becc-136">La fonction **CoCreateInstance** retourne **RegDB \_ E \_ CLASSNOTREG** si la classe n’est pas inscrite.</span><span class="sxs-lookup"><span data-stu-id="6becc-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="6becc-137">Version de BITS</span><span class="sxs-lookup"><span data-stu-id="6becc-137">BITS version</span></span>  | <span data-ttu-id="6becc-138">Identificateur de classe symbolique</span><span class="sxs-lookup"><span data-stu-id="6becc-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="6becc-139">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="6becc-139">BITS 10.1</span></span>     | <span data-ttu-id="6becc-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6becc-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="6becc-141">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="6becc-141">BITS 5.0</span></span>      | <span data-ttu-id="6becc-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6becc-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="6becc-143">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="6becc-143">BITS 4.0</span></span>      | <span data-ttu-id="6becc-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6becc-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="6becc-145">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="6becc-145">BITS 3.0</span></span>      | <span data-ttu-id="6becc-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6becc-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="6becc-147">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="6becc-147">BITS 2.5</span></span>      | <span data-ttu-id="6becc-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="6becc-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="6becc-149">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="6becc-149">BITS 2.0</span></span>      | <span data-ttu-id="6becc-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6becc-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="6becc-151">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="6becc-151">BITS 1.5</span></span>      | <span data-ttu-id="6becc-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="6becc-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="6becc-153">BITS 1,2, 1,0</span><span class="sxs-lookup"><span data-stu-id="6becc-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="6becc-154">CLSID \_ BackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="6becc-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




