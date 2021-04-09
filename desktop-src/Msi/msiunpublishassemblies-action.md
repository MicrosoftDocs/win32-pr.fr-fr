---
description: L’action MsiUnpublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32 en cours de suppression.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Action MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867469"
---
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="565f3-103">Action MsiUnpublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="565f3-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="565f3-104">L’action MsiUnpublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32 en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="565f3-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="565f3-105">L’action interroge la [table MsiAssembly](msiassembly-table.md) pour déterminer les assemblys pour lesquels des fonctionnalités publiées ou installées ont été supprimées de la global assembly cache et quels assemblys ont un composant parent publié ou installé en cours de suppression d’un emplacement isolé pour une application particulière.</span><span class="sxs-lookup"><span data-stu-id="565f3-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="565f3-106">Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="565f3-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="565f3-107">Sur les systèmes exécutant Windows XP et versions ultérieures, Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="565f3-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="565f3-108">Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="565f3-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="565f3-109">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="565f3-109">Sequence Restrictions</span></span>

<span data-ttu-id="565f3-110">L’action MsiUnpublishAssemblies doit venir après l' [action InstallInitialize](installinitialize-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="565f3-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="565f3-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="565f3-111">ActionData Messages</span></span>



| <span data-ttu-id="565f3-112">Champ</span><span class="sxs-lookup"><span data-stu-id="565f3-112">Field</span></span> | <span data-ttu-id="565f3-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="565f3-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="565f3-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="565f3-114">\[1\]</span></span> | <span data-ttu-id="565f3-115">Contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="565f3-115">Application context.</span></span>       |
| <span data-ttu-id="565f3-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="565f3-116">\[2\]</span></span> | <span data-ttu-id="565f3-117">Nom de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="565f3-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="565f3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="565f3-118">Remarks</span></span>

<span data-ttu-id="565f3-119">L' [action MsiPublishAssemblies](msipublishassemblies-action.md) gère la publication des assemblys publiés ou installés.</span><span class="sxs-lookup"><span data-stu-id="565f3-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
