---
title: Structures et fonctions d’assistance pour D3D12
description: Ces structures d’assistance et fonctions d’assistance sont déclarées dans d3dx12. h.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Fonctions d’assistance
- Structures d’assistance
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517960"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="e6492-106">Structures et fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="e6492-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="e6492-107">Ces structures d’assistance et fonctions d’assistance sont déclarées dans **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="e6492-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="e6492-108">Vous pouvez utiliser ces structures d’assistance pour créer et initialiser des structures Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e6492-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="e6492-109">Ces structures d’assistance se comportent comme des classes C++.</span><span class="sxs-lookup"><span data-stu-id="e6492-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="e6492-110">Chaque structure d’assistance a généralement un constructeur par défaut, un constructeur explicite, un destructeur et un opérateur de cast pour la structure D3D12 associée.</span><span class="sxs-lookup"><span data-stu-id="e6492-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="e6492-111">Chaque structure d’assistance a un préfixe « C » et est associée à une structure D3D12 qui ne possède pas le préfixe « C ».</span><span class="sxs-lookup"><span data-stu-id="e6492-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="e6492-112">La plupart des structures d’assistance contiennent des méthodes membres d’initialisation, certaines contiennent des fonctions de comparaison.</span><span class="sxs-lookup"><span data-stu-id="e6492-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="e6492-113">**d3dx12. h** est disponible séparément des en-têtes Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e6492-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="e6492-114">Vous pouvez télécharger **d3dx12. h** à partir de [la bibliothèque d’assistance D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span><span class="sxs-lookup"><span data-stu-id="e6492-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e6492-115">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e6492-115">In this section</span></span>



| <span data-ttu-id="e6492-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e6492-116">Topic</span></span>                                                                     | <span data-ttu-id="e6492-117">Description</span><span class="sxs-lookup"><span data-stu-id="e6492-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6492-118">Interfaces d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="e6492-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="e6492-119">Ces interfaces d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="e6492-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="e6492-120">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="e6492-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="e6492-121">Ces structures d’assistance permettent d’initialiser un grand nombre des structures Direct3D 12 et sont déclarées dans **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="e6492-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="e6492-122">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="e6492-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="e6492-123">Ces fonctions d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="e6492-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e6492-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6492-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6492-125">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e6492-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





