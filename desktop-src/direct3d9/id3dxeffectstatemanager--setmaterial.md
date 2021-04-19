---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état du matériau.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager :: SetMaterial, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542171"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="be9e3-103">ID3DXEffectStateManager :: SetMaterial, méthode</span><span class="sxs-lookup"><span data-stu-id="be9e3-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="be9e3-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état du matériau.</span><span class="sxs-lookup"><span data-stu-id="be9e3-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be9e3-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="be9e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be9e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be9e3-107">*pMaterial* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be9e3-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9e3-108">Type : **const [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="be9e3-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="be9e3-109">Pointeur vers l’état du matériau.</span><span class="sxs-lookup"><span data-stu-id="be9e3-109">A pointer to the material state.</span></span> <span data-ttu-id="be9e3-110">Consultez [**D3DMATERIAL9**](d3dmaterial9.md).</span><span class="sxs-lookup"><span data-stu-id="be9e3-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be9e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be9e3-111">Return value</span></span>

<span data-ttu-id="be9e3-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be9e3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be9e3-113">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be9e3-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="be9e3-114">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="be9e3-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="be9e3-115">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="be9e3-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="be9e3-116">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) échouera.</span><span class="sxs-lookup"><span data-stu-id="be9e3-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9e3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be9e3-117">Requirements</span></span>



| <span data-ttu-id="be9e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be9e3-118">Requirement</span></span> | <span data-ttu-id="be9e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="be9e3-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9e3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="be9e3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="be9e3-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9e3-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="be9e3-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be9e3-122">Library</span></span><br/> | <dl> <span data-ttu-id="be9e3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be9e3-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="be9e3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be9e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9e3-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="be9e3-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
