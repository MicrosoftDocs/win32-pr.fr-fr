---
description: 'ID3DXEffectStateManager :: SetVertexShaderConstantI, méthode-fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes entières de nuanceur de sommets.'
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'ID3DXEffectStateManager :: SetVertexShaderConstantI, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c129e3e01fe6fbae6ba7ede1b9ea8c4bee5338a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090397"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="ed687-103">ID3DXEffectStateManager :: SetVertexShaderConstantI, méthode</span><span class="sxs-lookup"><span data-stu-id="ed687-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="ed687-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes entières de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="ed687-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed687-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed687-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="ed687-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed687-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed687-107">*StartRegister* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed687-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed687-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed687-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed687-109">Index de base zéro du premier registre constant.</span><span class="sxs-lookup"><span data-stu-id="ed687-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="ed687-110">*pConstantData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed687-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed687-111">Type : **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ed687-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed687-112">Tableau de constantes entières.</span><span class="sxs-lookup"><span data-stu-id="ed687-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="ed687-113">*RegisterCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed687-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed687-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed687-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed687-115">Nombre de registres dans pConstantData.</span><span class="sxs-lookup"><span data-stu-id="ed687-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed687-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ed687-116">Return value</span></span>

<span data-ttu-id="ed687-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed687-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed687-118">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed687-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="ed687-119">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="ed687-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="ed687-120">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="ed687-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="ed687-121">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) échouera.</span><span class="sxs-lookup"><span data-stu-id="ed687-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed687-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed687-122">Requirements</span></span>



| <span data-ttu-id="ed687-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed687-123">Requirement</span></span> | <span data-ttu-id="ed687-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed687-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed687-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed687-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ed687-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed687-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ed687-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ed687-127">Library</span></span><br/> | <dl> <span data-ttu-id="ed687-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed687-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ed687-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed687-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed687-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="ed687-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
