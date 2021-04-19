---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de l’étape de texture.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'ID3DXEffectStateManager :: SetTextureStageState, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538346"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="3299e-103">ID3DXEffectStateManager :: SetTextureStageState, méthode</span><span class="sxs-lookup"><span data-stu-id="3299e-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="3299e-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de l’étape de texture.</span><span class="sxs-lookup"><span data-stu-id="3299e-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3299e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3299e-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="3299e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3299e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3299e-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3299e-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3299e-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3299e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3299e-109">Étape à laquelle la texture est assignée.</span><span class="sxs-lookup"><span data-stu-id="3299e-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="3299e-110">Il s’agit de la valeur d’index dans [**IDirect3DDevice9 :: SetTexture**](/windows/desktop/api) ou [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="3299e-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="3299e-111">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3299e-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3299e-112">Type : **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="3299e-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="3299e-113">Définit le type d’opération que doit effectuer une étape de texture.</span><span class="sxs-lookup"><span data-stu-id="3299e-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="3299e-114">Consultez [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="3299e-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3299e-115">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3299e-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3299e-116">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3299e-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3299e-117">Il peut s’agir d’une opération ([**D3DTEXTUREOP**](./d3dtextureop.md)) ou d’une valeur d’argument ([D3DTA](d3dta.md)), en fonction de ce qui est choisi pour le type.</span><span class="sxs-lookup"><span data-stu-id="3299e-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3299e-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3299e-118">Return value</span></span>

<span data-ttu-id="3299e-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3299e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3299e-120">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3299e-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="3299e-121">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="3299e-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="3299e-122">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="3299e-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="3299e-123">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) échouera.</span><span class="sxs-lookup"><span data-stu-id="3299e-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="3299e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3299e-124">Requirements</span></span>



| <span data-ttu-id="3299e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3299e-125">Requirement</span></span> | <span data-ttu-id="3299e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3299e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3299e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3299e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3299e-128"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3299e-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3299e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3299e-129">Library</span></span><br/> | <dl> <span data-ttu-id="3299e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3299e-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3299e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3299e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3299e-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="3299e-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
