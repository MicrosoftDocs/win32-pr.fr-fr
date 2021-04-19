---
description: Obtient un jeu d’animations en fonction de son nom.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController :: GetAnimationSetByName, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531560"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="4bf28-103">ID3DXAnimationController :: GetAnimationSetByName, méthode</span><span class="sxs-lookup"><span data-stu-id="4bf28-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="4bf28-104">Obtient un jeu d’animations en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="4bf28-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bf28-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="4bf28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bf28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf28-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bf28-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf28-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf28-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bf28-109">Chaîne contenant le nom de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="4bf28-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="4bf28-110">*ppAnimSet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4bf28-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf28-111">Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="4bf28-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="4bf28-112">Pointeur vers le jeu d’animations [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="4bf28-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf28-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bf28-113">Return value</span></span>

<span data-ttu-id="4bf28-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4bf28-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4bf28-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4bf28-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4bf28-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4bf28-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf28-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4bf28-117">Remarks</span></span>

<span data-ttu-id="4bf28-118">Le contrôleur d’animation contient un tableau d’ensembles d’animations.</span><span class="sxs-lookup"><span data-stu-id="4bf28-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="4bf28-119">Cette méthode retourne un jeu d’animations qui porte le nom donné.</span><span class="sxs-lookup"><span data-stu-id="4bf28-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf28-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bf28-120">Requirements</span></span>



| <span data-ttu-id="4bf28-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bf28-121">Requirement</span></span> | <span data-ttu-id="4bf28-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bf28-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf28-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bf28-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4bf28-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf28-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4bf28-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4bf28-125">Library</span></span><br/> | <dl> <span data-ttu-id="4bf28-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf28-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bf28-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bf28-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf28-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4bf28-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
