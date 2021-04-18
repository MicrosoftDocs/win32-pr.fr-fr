---
description: Définissez les informations de traduction pour une image clé spécifique dans l’ensemble d’animations.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'ID3DXKeyframedAnimationSet :: SetTranslationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520349"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a><span data-ttu-id="bf490-103">ID3DXKeyframedAnimationSet :: SetTranslationKey, méthode</span><span class="sxs-lookup"><span data-stu-id="bf490-103">ID3DXKeyframedAnimationSet::SetTranslationKey method</span></span>

<span data-ttu-id="bf490-104">Définissez les informations de traduction pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="bf490-104">Set translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf490-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf490-105">Syntax</span></span>


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="bf490-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf490-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf490-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf490-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf490-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf490-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf490-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="bf490-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="bf490-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf490-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf490-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf490-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf490-112">Image clé.</span><span class="sxs-lookup"><span data-stu-id="bf490-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="bf490-113">*pTranslationKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf490-113">*pTranslationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf490-114">Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="bf490-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="bf490-115">Pointeur vers les données de traduction.</span><span class="sxs-lookup"><span data-stu-id="bf490-115">Pointer to the translation data.</span></span> <span data-ttu-id="bf490-116">Consultez [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="bf490-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf490-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf490-117">Return value</span></span>

<span data-ttu-id="bf490-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf490-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf490-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf490-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf490-120">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bf490-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf490-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf490-121">Requirements</span></span>



| <span data-ttu-id="bf490-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf490-122">Requirement</span></span> | <span data-ttu-id="bf490-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf490-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf490-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf490-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bf490-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf490-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bf490-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf490-126">Library</span></span><br/> | <dl> <span data-ttu-id="bf490-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf490-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf490-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf490-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf490-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="bf490-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
