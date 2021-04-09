---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de sommets.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'ID3DXEffectStateManager :: SetVertexShader, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870158"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a><span data-ttu-id="00dd9-103">ID3DXEffectStateManager :: SetVertexShader, méthode</span><span class="sxs-lookup"><span data-stu-id="00dd9-103">ID3DXEffectStateManager::SetVertexShader method</span></span>

<span data-ttu-id="00dd9-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="00dd9-104">A callback function that must be implemented by a user to set a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="00dd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00dd9-105">Syntax</span></span>


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="00dd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00dd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00dd9-107">*pShader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00dd9-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dd9-108">Type : **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span><span class="sxs-lookup"><span data-stu-id="00dd9-108">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span></span>

<span data-ttu-id="00dd9-109">Pointeur vers un objet de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="00dd9-109">A pointer to a vertex shader object.</span></span> <span data-ttu-id="00dd9-110">Consultez [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="00dd9-110">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00dd9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00dd9-111">Return value</span></span>

<span data-ttu-id="00dd9-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00dd9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00dd9-113">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="00dd9-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="00dd9-114">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="00dd9-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="00dd9-115">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="00dd9-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="00dd9-116">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) échouera.</span><span class="sxs-lookup"><span data-stu-id="00dd9-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="00dd9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00dd9-117">Requirements</span></span>



| <span data-ttu-id="00dd9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00dd9-118">Requirement</span></span> | <span data-ttu-id="00dd9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="00dd9-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00dd9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="00dd9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="00dd9-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="00dd9-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="00dd9-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00dd9-122">Library</span></span><br/> | <dl> <span data-ttu-id="00dd9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00dd9-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="00dd9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00dd9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dd9-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="00dd9-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
