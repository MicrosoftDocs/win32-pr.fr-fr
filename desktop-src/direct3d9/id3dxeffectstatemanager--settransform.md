---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir une transformation.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'ID3DXEffectStateManager :: SetTransform, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953912"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="3c018-103">ID3DXEffectStateManager :: SetTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="3c018-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="3c018-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir une transformation.</span><span class="sxs-lookup"><span data-stu-id="3c018-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c018-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c018-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="3c018-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c018-107">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c018-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c018-108">Type : **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="3c018-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="3c018-109">Type de transformation à appliquer à la matrice.</span><span class="sxs-lookup"><span data-stu-id="3c018-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="3c018-110">Consultez [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="3c018-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c018-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c018-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c018-112">Type : **const [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c018-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="3c018-113">Matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="3c018-113">A transformation matrix.</span></span> <span data-ttu-id="3c018-114">Consultez [**D3DMATRIX**](d3dmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3c018-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c018-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c018-115">Return value</span></span>

<span data-ttu-id="3c018-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c018-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c018-117">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c018-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="3c018-118">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="3c018-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="3c018-119">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="3c018-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="3c018-120">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) échouera.</span><span class="sxs-lookup"><span data-stu-id="3c018-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c018-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c018-121">Requirements</span></span>



| <span data-ttu-id="3c018-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c018-122">Requirement</span></span> | <span data-ttu-id="3c018-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c018-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c018-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c018-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3c018-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c018-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3c018-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c018-126">Library</span></span><br/> | <dl> <span data-ttu-id="3c018-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c018-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3c018-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c018-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c018-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="3c018-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
