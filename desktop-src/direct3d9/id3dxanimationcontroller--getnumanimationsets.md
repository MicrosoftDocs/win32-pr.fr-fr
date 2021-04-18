---
description: Retourne le nombre de jeux d’animations actuellement enregistrés dans le contrôleur d’animation.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController :: GetNumAnimationSets, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522567"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="fb9d6-103">ID3DXAnimationController :: GetNumAnimationSets, méthode</span><span class="sxs-lookup"><span data-stu-id="fb9d6-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="fb9d6-104">Retourne le nombre de jeux d’animations actuellement enregistrés dans le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="fb9d6-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9d6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb9d6-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="fb9d6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb9d6-106">Parameters</span></span>

<span data-ttu-id="fb9d6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fb9d6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb9d6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb9d6-108">Return value</span></span>

<span data-ttu-id="fb9d6-109">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9d6-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb9d6-110">Nombre d’ensembles d’animations.</span><span class="sxs-lookup"><span data-stu-id="fb9d6-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb9d6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fb9d6-111">Remarks</span></span>

<span data-ttu-id="fb9d6-112">Le contrôleur contient un nombre quelconque d’animations et de jeux d’animations.</span><span class="sxs-lookup"><span data-stu-id="fb9d6-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="fb9d6-113">Les jeux d’animations peuvent être enregistrés avec [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span><span class="sxs-lookup"><span data-stu-id="fb9d6-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="fb9d6-114">Un contrôleur d’animation créé par un appel à [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) inscrit automatiquement les jeux d’animations chargés.</span><span class="sxs-lookup"><span data-stu-id="fb9d6-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9d6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb9d6-115">Requirements</span></span>



| <span data-ttu-id="fb9d6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb9d6-116">Requirement</span></span> | <span data-ttu-id="fb9d6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb9d6-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9d6-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb9d6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fb9d6-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9d6-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fb9d6-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb9d6-120">Library</span></span><br/> | <dl> <span data-ttu-id="fb9d6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb9d6-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb9d6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb9d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9d6-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="fb9d6-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
