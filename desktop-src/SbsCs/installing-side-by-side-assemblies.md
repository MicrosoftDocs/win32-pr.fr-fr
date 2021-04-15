---
description: Vous pouvez installer des assemblys côte à côte en tant qu’assemblys partagés ou en tant qu’assemblys privés. Pour plus d’informations, consultez Installation d’assemblys côte à côte en tant qu’assemblys privés et installation d’assemblys côte à côte en tant qu’assemblys partagés.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Installation d’assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484640"
---
# <a name="installing-side-by-side-assemblies"></a><span data-ttu-id="269e0-104">Installation d’assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="269e0-104">Installing Side-by-side Assemblies</span></span>

<span data-ttu-id="269e0-105">Vous pouvez installer des assemblys côte à côte en tant qu’assemblys [partagés](/windows/desktop/Msi/shared-assemblies) ou en tant qu' [assemblys privés](/windows/desktop/Msi/private-assemblies).</span><span class="sxs-lookup"><span data-stu-id="269e0-105">You may install side-by-side assemblies as [shared assemblies](/windows/desktop/Msi/shared-assemblies) or as [private assemblies](/windows/desktop/Msi/private-assemblies).</span></span> <span data-ttu-id="269e0-106">Pour plus d’informations, consultez [installation d’assemblys côte à côte en tant qu’assemblys privés](installing-side-by-side-assemblies-as-private-assemblies.md) et [installation d’assemblys côte à côte en tant qu’assemblys partagés](installing-side-by-side-assemblies-as-shared-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="269e0-106">For more information, see [Installing Side-by-Side Assemblies as Private Assemblies](installing-side-by-side-assemblies-as-private-assemblies.md) and [Installing Side-by-side Assemblies as Shared Assemblies](installing-side-by-side-assemblies-as-shared-assemblies.md).</span></span>

<span data-ttu-id="269e0-107">Notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="269e0-107">Note that:</span></span>

-   <span data-ttu-id="269e0-108">Les assemblys installés dans le Global Assembly Cache par une installation à l’aide du [contexte d’installation](/windows/desktop/Msi/installation-context) par utilisateur ne sont pas protégés par la protection des fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="269e0-108">Assemblies installed to the global assembly cache by an installation using the per-user [installation context](/windows/desktop/Msi/installation-context) are not protected by Windows File Protection.</span></span>
-   <span data-ttu-id="269e0-109">Les assemblys installés dans le Global Assembly Cache par une installation à l’aide du contexte d' [installation](/windows/desktop/Msi/installation-context) par ordinateur sont protégés par la protection des fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="269e0-109">Assemblies that are installed to the global assembly cache by an installation using the per-machine [installation context](/windows/desktop/Msi/installation-context) are protected by Windows File Protection.</span></span>

 

 
