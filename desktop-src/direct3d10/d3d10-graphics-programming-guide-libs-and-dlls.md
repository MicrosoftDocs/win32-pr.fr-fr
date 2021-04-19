---
description: Pour qu’une application s’exécute correctement, les dll appropriées doivent être installées sur l’ordinateur hôte. Ces dll peuvent être fournies par le système d’exploitation ou le package redistribuable des applications.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Liaison de bibliothèques statiques et dynamiques (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513929"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="8972f-104">Liaison de bibliothèques statiques et dynamiques (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8972f-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="8972f-105">Pour qu’une application s’exécute correctement, les dll appropriées doivent être installées sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="8972f-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="8972f-106">Ces dll peuvent être fournies par le système d’exploitation ou le package redistribuable des applications.</span><span class="sxs-lookup"><span data-stu-id="8972f-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="8972f-107">Les bibliothèques chargent les dll appropriées</span><span class="sxs-lookup"><span data-stu-id="8972f-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="8972f-108">Les bibliothèques incluses avec le kit de développement logiciel (SDK) DirectX chargent automatiquement les dll appropriées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="8972f-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="8972f-109">L’exception à cette règle est d3dx10. lib/d3dx10d. lib, qui chargera le d3dx10.dll fourni avec cette version du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="8972f-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="8972f-110">Par exemple, si le kit de développement logiciel (SDK) téléchargé comprend d3dx10 \_33.dll et d3dx10 \_34.dll, la bibliothèque (d3dx10. lib) fournie avec ce kit de développement logiciel (SDK) charge d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="8972f-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="8972f-111">Si un kit de développement logiciel (SDK) suivant est installé ultérieurement avec d3dx10 \_ 35. lib, le d3dx10. lib du SDK précédent chargera toujours d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="8972f-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="8972f-112">Le d3dx10. lib du kit de développement logiciel (SDK) le plus récent chargera d3dx10 \_35.dll.</span><span class="sxs-lookup"><span data-stu-id="8972f-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="8972f-113">Redistribution des binaires</span><span class="sxs-lookup"><span data-stu-id="8972f-113">Redistributing Binaries</span></span>

<span data-ttu-id="8972f-114">Seules les d3dx10.dll (et les versions ultérieures du même fichier) peuvent être redistribuées.</span><span class="sxs-lookup"><span data-stu-id="8972f-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="8972f-115">Pour redistribuer ce fichier, vous devez utiliser la fonction **DirectXSetup** .</span><span class="sxs-lookup"><span data-stu-id="8972f-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="8972f-116">Pour plus d’informations sur l’utilisation de cette fonction et la combinaison d’un package redistribuable, consultez [installation de DirectX avec DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8972f-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="8972f-117">Tous les autres fichiers binaires nécessaires sont inclus dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8972f-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="8972f-118">Les seuls fichiers binaires qui peuvent être redistribués sont ceux qui se trouvent dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="8972f-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="8972f-119">Le tableau suivant décrit les binaires que les développeurs doivent connaître.</span><span class="sxs-lookup"><span data-stu-id="8972f-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="8972f-120">Fichiers binaires Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="8972f-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="8972f-121">Description</span><span class="sxs-lookup"><span data-stu-id="8972f-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8972f-122">d3dx10.dll/d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="8972f-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="8972f-123">Composants D3DX10 des versions commerciales et de débogage ; les composants de la version commerciale peuvent être redistribués dans le CAB Redist.</span><span class="sxs-lookup"><span data-stu-id="8972f-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8972f-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="8972f-124">d3d10ref.dll</span></span>           | <span data-ttu-id="8972f-125">Rastériseur de référence.</span><span class="sxs-lookup"><span data-stu-id="8972f-125">Reference Rasterizer.</span></span> <span data-ttu-id="8972f-126">Fournit une implémentation logicielle du pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="8972f-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="8972f-127">Inclus uniquement dans le cadre de la SDK Windows ou du SDK DirectX hérité et ne peut pas être redistribué.</span><span class="sxs-lookup"><span data-stu-id="8972f-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="8972f-128">Le rastériseur de référence est destiné uniquement au débogage.</span><span class="sxs-lookup"><span data-stu-id="8972f-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="8972f-129">La liaison explicite n’est pas nécessaire. toute tentative de création d’un appareil de référence (voir [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) chargera cette dll si elle est présente.</span><span class="sxs-lookup"><span data-stu-id="8972f-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="8972f-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="8972f-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="8972f-131">Série d’utilitaires SDK qui agit comme une couche entre les appels d’API et l’exécution du runtime, y compris la couche de [débogage](d3d10-graphics-programming-guide-api-features-layers.md) et la couche Switch-to-Reference.</span><span class="sxs-lookup"><span data-stu-id="8972f-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="8972f-132">La liaison explicite n’est pas nécessaire. Si un appareil est créé avec l’indicateur de couche approprié, cette DLL est chargée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8972f-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="8972f-133">Ce composant est destiné uniquement à des fins de développement et de débogage.</span><span class="sxs-lookup"><span data-stu-id="8972f-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="8972f-134">Inclus uniquement dans le cadre de la SDK Windows ou du SDK DirectX hérité et ne peut pas être redistribué.</span><span class="sxs-lookup"><span data-stu-id="8972f-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8972f-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8972f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8972f-136">Guide de programmation pour Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="8972f-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="8972f-137">Graphiques Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="8972f-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



