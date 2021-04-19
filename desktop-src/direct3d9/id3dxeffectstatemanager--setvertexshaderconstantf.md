---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'ID3DXEffectStateManager :: SetVertexShaderConstantF, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 378af983e0ed7ca1709ae8bb6cfe8615a481b3f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529622"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="c5a08-103">ID3DXEffectStateManager :: SetVertexShaderConstantF, méthode</span><span class="sxs-lookup"><span data-stu-id="c5a08-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="c5a08-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c5a08-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a08-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5a08-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="c5a08-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5a08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a08-107">*StartRegister* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c5a08-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5a08-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5a08-109">Index de base zéro du premier registre constant.</span><span class="sxs-lookup"><span data-stu-id="c5a08-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-110">*pConstantData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c5a08-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5a08-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c5a08-112">Tableau de constantes à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c5a08-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-113">*RegisterCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c5a08-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5a08-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5a08-115">Nombre de registres dans pConstantData.</span><span class="sxs-lookup"><span data-stu-id="c5a08-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a08-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5a08-116">Return value</span></span>

<span data-ttu-id="c5a08-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5a08-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5a08-118">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5a08-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c5a08-119">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="c5a08-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="c5a08-120">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="c5a08-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="c5a08-121">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) échouera.</span><span class="sxs-lookup"><span data-stu-id="c5a08-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a08-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5a08-122">Requirements</span></span>



| <span data-ttu-id="c5a08-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5a08-123">Requirement</span></span> | <span data-ttu-id="c5a08-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5a08-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a08-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5a08-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c5a08-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a08-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c5a08-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5a08-127">Library</span></span><br/> | <dl> <span data-ttu-id="c5a08-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5a08-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5a08-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5a08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a08-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="c5a08-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
