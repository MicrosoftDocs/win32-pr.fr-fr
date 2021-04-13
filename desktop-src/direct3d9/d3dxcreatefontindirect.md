---
description: Crée un objet de police indirectement pour un appareil et une police.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: D3DXCreateFontIndirect, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323161"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="23841-103">D3DXCreateFontIndirect fonction)</span><span class="sxs-lookup"><span data-stu-id="23841-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="23841-104">Crée un objet de police indirectement pour un appareil et une police.</span><span class="sxs-lookup"><span data-stu-id="23841-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="23841-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23841-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="23841-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23841-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23841-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23841-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="23841-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="23841-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’appareil à associer à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="23841-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="23841-110">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23841-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23841-111">Type : **const [**D3DXFONT \_ desc**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="23841-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="23841-112">Pointeur vers une structure [**D3DXFONT \_ desc**](d3dxfont-desc.md) , décrivant les attributs de l’objet font à créer.</span><span class="sxs-lookup"><span data-stu-id="23841-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="23841-113">Si les paramètres du compilateur requièrent Unicode, le type de données D3DXFONT \_ desc correspond à D3DXFONT \_ DESCW ; dans le cas contraire, le type de données est résolu en D3DXFONT \_ DESCA.</span><span class="sxs-lookup"><span data-stu-id="23841-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="23841-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="23841-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="23841-115">*ppFont* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="23841-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23841-116">Type : **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="23841-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="23841-117">Retourne un pointeur vers une interface [**ID3DXFont**](id3dxfont.md) représentant l’objet de police créé.</span><span class="sxs-lookup"><span data-stu-id="23841-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23841-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23841-118">Return value</span></span>

<span data-ttu-id="23841-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23841-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23841-120">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23841-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23841-121">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="23841-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="23841-122">Notes</span><span class="sxs-lookup"><span data-stu-id="23841-122">Remarks</span></span>

<span data-ttu-id="23841-123">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="23841-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="23841-124">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="23841-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="23841-125">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontIndirectA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="23841-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="23841-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23841-126">Requirements</span></span>



| <span data-ttu-id="23841-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23841-127">Requirement</span></span> | <span data-ttu-id="23841-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="23841-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23841-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="23841-129">Header</span></span><br/>  | <dl> <span data-ttu-id="23841-130"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="23841-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="23841-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23841-131">Library</span></span><br/> | <dl> <span data-ttu-id="23841-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23841-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23841-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23841-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23841-134">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="23841-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
