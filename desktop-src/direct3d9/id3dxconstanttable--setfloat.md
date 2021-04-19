---
description: Définit un nombre à virgule flottante.
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'ID3DXConstantTable :: SetFloat, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535180"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="ac85b-103">ID3DXConstantTable :: SetFloat, méthode</span><span class="sxs-lookup"><span data-stu-id="ac85b-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="ac85b-104">Définit un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="ac85b-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac85b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac85b-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="ac85b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac85b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac85b-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac85b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac85b-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ac85b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ac85b-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="ac85b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="ac85b-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac85b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac85b-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ac85b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ac85b-112">Identificateur unique de la constante.</span><span class="sxs-lookup"><span data-stu-id="ac85b-112">Unique identifier to the constant.</span></span> <span data-ttu-id="ac85b-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ac85b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac85b-114">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac85b-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac85b-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac85b-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac85b-116">Nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="ac85b-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac85b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac85b-117">Return value</span></span>

<span data-ttu-id="ac85b-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac85b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac85b-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac85b-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac85b-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ac85b-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac85b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac85b-121">Requirements</span></span>



| <span data-ttu-id="ac85b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac85b-122">Requirement</span></span> | <span data-ttu-id="ac85b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac85b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac85b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac85b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ac85b-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac85b-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ac85b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac85b-126">Library</span></span><br/> | <dl> <span data-ttu-id="ac85b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac85b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ac85b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac85b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac85b-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ac85b-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
