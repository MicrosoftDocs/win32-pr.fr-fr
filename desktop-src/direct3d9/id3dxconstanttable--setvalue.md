---
description: Définit le contenu de la mémoire tampon sur la table constante.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'ID3DXConstantTable :: SetValue, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538516"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="845a7-103">ID3DXConstantTable :: SetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="845a7-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="845a7-104">Définit le contenu de la mémoire tampon sur la table constante.</span><span class="sxs-lookup"><span data-stu-id="845a7-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="845a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="845a7-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="845a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="845a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="845a7-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="845a7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a7-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="845a7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="845a7-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="845a7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="845a7-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="845a7-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a7-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="845a7-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="845a7-112">Identificateur unique d’une constante.</span><span class="sxs-lookup"><span data-stu-id="845a7-112">Unique identifier to a constant.</span></span> <span data-ttu-id="845a7-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="845a7-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="845a7-114">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="845a7-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a7-115">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="845a7-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="845a7-116">Mémoire tampon contenant les données.</span><span class="sxs-lookup"><span data-stu-id="845a7-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="845a7-117">*Octets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="845a7-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a7-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="845a7-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="845a7-119">Taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="845a7-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="845a7-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="845a7-120">Return value</span></span>

<span data-ttu-id="845a7-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="845a7-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="845a7-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="845a7-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="845a7-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="845a7-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="845a7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="845a7-124">Requirements</span></span>



| <span data-ttu-id="845a7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="845a7-125">Requirement</span></span> | <span data-ttu-id="845a7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="845a7-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="845a7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="845a7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="845a7-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="845a7-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="845a7-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="845a7-129">Library</span></span><br/> | <dl> <span data-ttu-id="845a7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="845a7-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="845a7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="845a7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="845a7-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="845a7-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
