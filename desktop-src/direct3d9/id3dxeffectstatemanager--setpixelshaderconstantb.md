---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: 'ID3DXEffectStateManager :: SetPixelShaderConstantB, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e3c3c988bdbfa84a3e815fe94d89c24f3fa3a264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531555"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a><span data-ttu-id="d5e6d-103">ID3DXEffectStateManager :: SetPixelShaderConstantB, méthode</span><span class="sxs-lookup"><span data-stu-id="d5e6d-103">ID3DXEffectStateManager::SetPixelShaderConstantB method</span></span>

<span data-ttu-id="d5e6d-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="d5e6d-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e6d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5e6d-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="d5e6d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5e6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e6d-107">*StartRegister* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5e6d-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e6d-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5e6d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5e6d-109">Index de base zéro du premier registre constant.</span><span class="sxs-lookup"><span data-stu-id="d5e6d-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="d5e6d-110">*pConstantData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5e6d-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e6d-111">Type : **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5e6d-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d5e6d-112">Tableau de constantes booléennes.</span><span class="sxs-lookup"><span data-stu-id="d5e6d-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="d5e6d-113">*RegisterCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5e6d-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e6d-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5e6d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5e6d-115">Nombre de registres dans pConstantData.</span><span class="sxs-lookup"><span data-stu-id="d5e6d-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e6d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5e6d-116">Return value</span></span>

<span data-ttu-id="d5e6d-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5e6d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5e6d-118">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5e6d-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="d5e6d-119">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="d5e6d-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="d5e6d-120">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="d5e6d-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="d5e6d-121">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) échouera.</span><span class="sxs-lookup"><span data-stu-id="d5e6d-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e6d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5e6d-122">Requirements</span></span>



| <span data-ttu-id="d5e6d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5e6d-123">Requirement</span></span> | <span data-ttu-id="d5e6d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e6d-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e6d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5e6d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5e6d-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e6d-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d5e6d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5e6d-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5e6d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5e6d-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d5e6d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5e6d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e6d-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="d5e6d-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
