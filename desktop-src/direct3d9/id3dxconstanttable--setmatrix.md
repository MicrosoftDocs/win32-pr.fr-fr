---
description: Définit une matrice nontransposed.
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: 'ID3DXConstantTable :: SetMatrix, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae227663a61087fae309d1954b8f0dc438f6df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522355"
---
# <a name="id3dxconstanttablesetmatrix-method"></a><span data-ttu-id="4f704-103">ID3DXConstantTable :: SetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="4f704-103">ID3DXConstantTable::SetMatrix method</span></span>

<span data-ttu-id="4f704-104">Définit une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="4f704-104">Sets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f704-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f704-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="4f704-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f704-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f704-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f704-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f704-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4f704-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4f704-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="4f704-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="4f704-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f704-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f704-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4f704-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4f704-112">Identificateur unique de la matrice de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f704-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="4f704-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4f704-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f704-114">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f704-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f704-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4f704-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4f704-116">Pointeur vers une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="4f704-116">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="4f704-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4f704-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f704-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f704-118">Return value</span></span>

<span data-ttu-id="4f704-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f704-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f704-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4f704-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4f704-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4f704-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f704-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f704-122">Requirements</span></span>



| <span data-ttu-id="4f704-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f704-123">Requirement</span></span> | <span data-ttu-id="4f704-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f704-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f704-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f704-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4f704-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f704-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4f704-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f704-127">Library</span></span><br/> | <dl> <span data-ttu-id="4f704-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f704-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4f704-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f704-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f704-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="4f704-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
