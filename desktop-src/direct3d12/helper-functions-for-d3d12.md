---
title: Fonctions d’assistance pour D3D12
description: Ces fonctions d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Fonctions d’assistance
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106522625"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="5b423-105">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="5b423-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="5b423-106">Ces fonctions d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="5b423-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5b423-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5b423-107">In this section</span></span>



| <span data-ttu-id="5b423-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5b423-108">Topic</span></span>                                                                                             | <span data-ttu-id="5b423-109">Description</span><span class="sxs-lookup"><span data-stu-id="5b423-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b423-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="5b423-110">**CommandListCast**</span></span>](cd3dx12-shader-bytecode.md)<br/>                                     | <span data-ttu-id="5b423-111">Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="5b423-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="5b423-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="5b423-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="5b423-113">Calcule un index de sous-ressource pour une texture.</span><span class="sxs-lookup"><span data-stu-id="5b423-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="5b423-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="5b423-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="5b423-115">Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié.</span><span class="sxs-lookup"><span data-stu-id="5b423-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="5b423-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="5b423-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="5b423-117">Obtient le nombre de plans pour le format DXGI spécifié pour la carte virtuelle spécifiée (un **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="5b423-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="5b423-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="5b423-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="5b423-119">Indique si la disposition est opaque.</span><span class="sxs-lookup"><span data-stu-id="5b423-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="5b423-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="5b423-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="5b423-121">Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé.</span><span class="sxs-lookup"><span data-stu-id="5b423-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="5b423-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="5b423-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="5b423-123">Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée.</span><span class="sxs-lookup"><span data-stu-id="5b423-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="5b423-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5b423-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="5b423-125">Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines.</span><span class="sxs-lookup"><span data-stu-id="5b423-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="5b423-126">Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5b423-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="5b423-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="5b423-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="5b423-128">Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données.</span><span class="sxs-lookup"><span data-stu-id="5b423-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="5b423-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="5b423-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="5b423-130">Copie une sous-ressource ligne par ligne.</span><span class="sxs-lookup"><span data-stu-id="5b423-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="5b423-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="5b423-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="5b423-132">Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="5b423-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="5b423-133">**Updatesubresources (allocation du tas)**</span><span class="sxs-lookup"><span data-stu-id="5b423-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="5b423-134">Met à jour les sous-ressources avec une implémentation d’allocation de tas.</span><span class="sxs-lookup"><span data-stu-id="5b423-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="5b423-135">**Updatesubresources (allocation de la pile)**</span><span class="sxs-lookup"><span data-stu-id="5b423-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="5b423-136">Met à jour les sous-ressources avec une implémentation d’allocation de pile.</span><span class="sxs-lookup"><span data-stu-id="5b423-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="5b423-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b423-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b423-138">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5b423-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="5b423-139">Structures et fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="5b423-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





