---
description: Les assemblys Common Language Runtime qui sont installés dans le Global Assembly Cache doivent avoir des fichiers identiques dans toutes les occurrences de l’assembly.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modes de réinstallation des assemblys du Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531928"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="ac4d8-103">Modes de réinstallation des assemblys du Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="ac4d8-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="ac4d8-104">Les assemblys Common Language Runtime qui sont installés dans le Global Assembly Cache doivent avoir des fichiers identiques dans toutes les occurrences de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="ac4d8-105">Cela signifie que les modes de réinstallation utilisés par [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) et [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) doivent avoir des significations différentes pour les composants normaux et les assemblys de Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="ac4d8-106">Les définitions de modes de réinstallation suivantes s’appliquent aux assemblys common language runtime.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="ac4d8-107">Mode de réinstallation</span><span class="sxs-lookup"><span data-stu-id="ac4d8-107">Reinstall mode</span></span>                  | <span data-ttu-id="ac4d8-108">Signification pour les composants Microsoft .NET</span><span class="sxs-lookup"><span data-stu-id="ac4d8-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4d8-109">REINSTALLMODE \_ FILEMISSING</span><span class="sxs-lookup"><span data-stu-id="ac4d8-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="ac4d8-110">Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="ac4d8-111">REINSTALLMODE \_ FILEOLDERVERSION</span><span class="sxs-lookup"><span data-stu-id="ac4d8-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="ac4d8-112">Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="ac4d8-113">REINSTALLMODE \_ FILEEQUALVERSION</span><span class="sxs-lookup"><span data-stu-id="ac4d8-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="ac4d8-114">Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="ac4d8-115">REINSTALLMODE \_ FILEEXACT</span><span class="sxs-lookup"><span data-stu-id="ac4d8-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="ac4d8-116">Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="ac4d8-117">REINSTALLMODE \_ FILEVERIFY</span><span class="sxs-lookup"><span data-stu-id="ac4d8-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="ac4d8-118">Installez ou réinstallez le composant common language runtime s’il est manquant ou si le composant existant est incomplet ou endommagé.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="ac4d8-119">REINSTALLMODE \_ FILEREPLACE</span><span class="sxs-lookup"><span data-stu-id="ac4d8-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="ac4d8-120">Installez ou réinstallez toujours le composant common language runtime.</span><span class="sxs-lookup"><span data-stu-id="ac4d8-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



