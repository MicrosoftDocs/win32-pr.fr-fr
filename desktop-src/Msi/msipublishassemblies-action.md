---
description: L’action MsiPublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Action MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532285"
---
# <a name="msipublishassemblies-action"></a><span data-ttu-id="4eca5-103">Action MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="4eca5-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="4eca5-104">L’action MsiPublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32.</span><span class="sxs-lookup"><span data-stu-id="4eca5-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="4eca5-105">L’action interroge la [table MsiAssembly](msiassembly-table.md) pour déterminer les assemblys qui ont des fonctionnalités publiées ou installées dans le global assembly cache et les assemblys dont le composant parent est publié ou installé dans un emplacement isolé pour une application particulière.</span><span class="sxs-lookup"><span data-stu-id="4eca5-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="4eca5-106">Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="4eca5-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="4eca5-107">Sur les systèmes Microsoft Windows XP et versions ultérieures, Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="4eca5-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="4eca5-108">Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="4eca5-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4eca5-109">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="4eca5-109">Sequence Restrictions</span></span>

<span data-ttu-id="4eca5-110">L’action MsiPublishAssemblies doit venir après l' [action InstallInitialize](installinitialize-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md) ou la [table AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4eca5-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4eca5-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="4eca5-111">ActionData Messages</span></span>



| <span data-ttu-id="4eca5-112">Champ</span><span class="sxs-lookup"><span data-stu-id="4eca5-112">Field</span></span> | <span data-ttu-id="4eca5-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="4eca5-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="4eca5-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4eca5-114">\[1\]</span></span> | <span data-ttu-id="4eca5-115">Contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="4eca5-115">Application context.</span></span>       |
| <span data-ttu-id="4eca5-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4eca5-116">\[2\]</span></span> | <span data-ttu-id="4eca5-117">Nom de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4eca5-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="4eca5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4eca5-118">Remarks</span></span>

<span data-ttu-id="4eca5-119">Pour plus d’informations, consultez [assemblys](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="4eca5-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="4eca5-120">L' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gère la publication des assemblys en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4eca5-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
