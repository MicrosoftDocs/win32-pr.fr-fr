---
description: Modules TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Modules TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034295"
---
# <a name="topoedit-modules"></a><span data-ttu-id="4f903-103">Modules TopoEdit</span><span class="sxs-lookup"><span data-stu-id="4f903-103">TopoEdit Modules</span></span>

<span data-ttu-id="4f903-104">L’outil TopoEdit est fourni avec le SDK Windows pour Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4f903-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="4f903-105">L’outil nécessite Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f903-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="4f903-106">Les modules TopoEdit se trouvent dans le dossier bin du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="4f903-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="4f903-107">Ces modules sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4f903-107">These modules are:</span></span>

-   <span data-ttu-id="4f903-108">TopoEdit.exe : exécutable de l’application</span><span class="sxs-lookup"><span data-stu-id="4f903-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="4f903-109">TEDUTIL.dll : DLL d’extension</span><span class="sxs-lookup"><span data-stu-id="4f903-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="4f903-110">L’installation du kit de développement logiciel (SDK) inscrit la DLL.</span><span class="sxs-lookup"><span data-stu-id="4f903-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="4f903-111">Toutefois, si cette opération échoue, à l’invite de commandes, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="4f903-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="4f903-112">Le code source pour TopoEdit est également fourni sous la forme d’un exemple dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="4f903-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="4f903-113">Il se trouve dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="4f903-113">It is located in the following directory:</span></span>

<span data-ttu-id="4f903-114"><samples root>\\\\TopoEdit multimédia Media Foundation \\</span><span class="sxs-lookup"><span data-stu-id="4f903-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f903-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f903-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f903-116">Présentation de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="4f903-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="4f903-117">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="4f903-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



