---
description: Obtient le handle d’une annotation.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect :: GetAnnotation, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538550"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="4f395-103">ID3DXBaseEffect :: GetAnnotation, méthode</span><span class="sxs-lookup"><span data-stu-id="4f395-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="4f395-104">Obtient le handle d’une annotation.</span><span class="sxs-lookup"><span data-stu-id="4f395-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f395-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f395-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="4f395-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f395-107">*hObject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f395-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f395-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4f395-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4f395-109">Handle d’une technique, d’un passe ou d’un paramètre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="4f395-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="4f395-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="4f395-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f395-111">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f395-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f395-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f395-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f395-113">Index d’annotation.</span><span class="sxs-lookup"><span data-stu-id="4f395-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f395-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f395-114">Return value</span></span>

<span data-ttu-id="4f395-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4f395-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4f395-116">Retourne le handle de l’annotation spécifiée, ou **null** si l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4f395-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="4f395-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="4f395-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f395-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4f395-118">Remarks</span></span>

<span data-ttu-id="4f395-119">Les annotations sont des données spécifiques à l’utilisateur qui peuvent être attachées à n’importe quelle technique, passe ou paramètre.</span><span class="sxs-lookup"><span data-stu-id="4f395-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="4f395-120">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="4f395-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f395-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f395-121">Requirements</span></span>



| <span data-ttu-id="4f395-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f395-122">Requirement</span></span> | <span data-ttu-id="4f395-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f395-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f395-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f395-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4f395-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f395-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4f395-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f395-126">Library</span></span><br/> | <dl> <span data-ttu-id="4f395-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f395-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4f395-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f395-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f395-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="4f395-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
