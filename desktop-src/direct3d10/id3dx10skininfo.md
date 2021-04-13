---
description: ID3DX10SkinInfo vous permet d’optimiser, de traiter et de définir manuellement la relation entre les segments et les vertex de vos mailles (voir animation de squelette sur Wikipédia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interface ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322949"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="96698-103">Interface ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="96698-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="96698-104">ID3DX10SkinInfo vous permet d’optimiser, de traiter et de définir manuellement la relation entre les segments et les vertex de vos mailles (voir [animation de squelette sur Wikipédia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span><span class="sxs-lookup"><span data-stu-id="96698-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="96698-105">Il est particulièrement utile pour créer des fichiers. x exportés par des applications DCC (telles que 3DS Max et Maya) plus compatibles avec le matériel et pour améliorer la vitesse de rendu de vos mailles dépouillées en mode de rendu logiciel.</span><span class="sxs-lookup"><span data-stu-id="96698-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="96698-106">Membres</span><span class="sxs-lookup"><span data-stu-id="96698-106">Members</span></span>

<span data-ttu-id="96698-107">L’interface **ID3DX10SkinInfo** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="96698-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="96698-108">**ID3DX10SkinInfo** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="96698-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="96698-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="96698-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="96698-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="96698-110">Methods</span></span>

<span data-ttu-id="96698-111">L’interface **ID3DX10SkinInfo** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="96698-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="96698-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="96698-112">Method</span></span>                                                                   | <span data-ttu-id="96698-113">Description</span><span class="sxs-lookup"><span data-stu-id="96698-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96698-114">**AddBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="96698-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="96698-115">Activez un segment existant pour influencer un groupe de vertex et définissez l’influence du segment sur chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="96698-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="96698-116">**AddBones**</span><span class="sxs-lookup"><span data-stu-id="96698-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="96698-117">Allouez de l’espace pour d’autres segments.</span><span class="sxs-lookup"><span data-stu-id="96698-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="96698-118">**AddVertices**</span><span class="sxs-lookup"><span data-stu-id="96698-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="96698-119">Allouez de l’espace pour des vertex supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="96698-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="96698-120">**ClearBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="96698-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="96698-121">Désactivez la liste des vertex d’un os qu’elle influence.</span><span class="sxs-lookup"><span data-stu-id="96698-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="96698-122">**Compact**</span><span class="sxs-lookup"><span data-stu-id="96698-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="96698-123">Limitez le nombre d’os pouvant influencer un vertex et/ou limitez la quantité d’influence qu’un segment peut avoir sur un sommet.</span><span class="sxs-lookup"><span data-stu-id="96698-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="96698-124">**DoSoftwareSkinning**</span><span class="sxs-lookup"><span data-stu-id="96698-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="96698-125">Effectuez des dépassements de logiciels sur un tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="96698-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="96698-126">**FindBoneInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="96698-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="96698-127">Recherche l’index qui indique où un vertex donné figure dans la liste des vertex influencés d’un segment donné.</span><span class="sxs-lookup"><span data-stu-id="96698-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="96698-128">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="96698-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="96698-129">Obtenir le degré d’influence d’un segment donné sur un vertex donné.</span><span class="sxs-lookup"><span data-stu-id="96698-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="96698-130">**GetBoneInfluenceCount**</span><span class="sxs-lookup"><span data-stu-id="96698-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="96698-131">Obtient le nombre de vertex qu’un segment donné influence.</span><span class="sxs-lookup"><span data-stu-id="96698-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="96698-132">**GetBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="96698-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="96698-133">Obtient la liste des vertex qu’un segment donné influence et une liste de la quantité d’influence que l’OS a sur chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="96698-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="96698-134">**GetMaxBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="96698-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="96698-135">Obtenir le nombre de vertex qu’un segment peut maximiser.</span><span class="sxs-lookup"><span data-stu-id="96698-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="96698-136">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="96698-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="96698-137">Obtient le nombre d’os dans ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="96698-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="96698-138">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="96698-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="96698-139">Obtient le nombre de vertex dans ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="96698-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="96698-140">**RemapBones**</span><span class="sxs-lookup"><span data-stu-id="96698-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="96698-141">Modifiez les segments qui influencent les vertex.</span><span class="sxs-lookup"><span data-stu-id="96698-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="96698-142">**RemapVertices**</span><span class="sxs-lookup"><span data-stu-id="96698-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="96698-143">Modifiez les vertex qui sont influencés par les segments.</span><span class="sxs-lookup"><span data-stu-id="96698-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="96698-144">**RemoveBone**</span><span class="sxs-lookup"><span data-stu-id="96698-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="96698-145">Supprimer un segment.</span><span class="sxs-lookup"><span data-stu-id="96698-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="96698-146">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="96698-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="96698-147">Définit le degré d’influence d’un segment donné sur un sommet donné.</span><span class="sxs-lookup"><span data-stu-id="96698-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="96698-148">Notes</span><span class="sxs-lookup"><span data-stu-id="96698-148">Remarks</span></span>

<span data-ttu-id="96698-149">Créez une interface ID3DX10SkinInfo avec [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** ou **D3DX10CreateSkinInfoFVF**.</span><span class="sxs-lookup"><span data-stu-id="96698-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="96698-150">Le type LPD3DX10SKININFO est défini comme un pointeur vers l’interface **ID3DX10SkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="96698-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="96698-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96698-151">Requirements</span></span>



| <span data-ttu-id="96698-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96698-152">Requirement</span></span> | <span data-ttu-id="96698-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="96698-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96698-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="96698-154">Header</span></span><br/>  | <dl> <span data-ttu-id="96698-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="96698-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="96698-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96698-156">Library</span></span><br/> | <dl> <span data-ttu-id="96698-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96698-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96698-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96698-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96698-159">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="96698-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
