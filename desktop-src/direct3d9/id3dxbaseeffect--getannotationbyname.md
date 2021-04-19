---
description: Obtient le handle d’une annotation en recherchant son nom.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'ID3DXBaseEffect :: GetAnnotationByName, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528578"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="1ba79-103">ID3DXBaseEffect :: GetAnnotationByName, méthode</span><span class="sxs-lookup"><span data-stu-id="1ba79-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="1ba79-104">Obtient le handle d’une annotation en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="1ba79-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba79-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ba79-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="1ba79-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ba79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba79-107">*hObject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ba79-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba79-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1ba79-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1ba79-109">Handle d’une technique, d’un passe ou d’un paramètre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="1ba79-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="1ba79-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1ba79-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ba79-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ba79-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba79-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ba79-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ba79-113">Chaîne contenant le nom de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="1ba79-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba79-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ba79-114">Return value</span></span>

<span data-ttu-id="1ba79-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1ba79-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1ba79-116">Retourne le handle de l’annotation spécifiée, ou **null** si le nom est introuvable.</span><span class="sxs-lookup"><span data-stu-id="1ba79-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="1ba79-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1ba79-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba79-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ba79-118">Requirements</span></span>



| <span data-ttu-id="1ba79-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ba79-119">Requirement</span></span> | <span data-ttu-id="1ba79-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ba79-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba79-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ba79-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1ba79-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ba79-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1ba79-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ba79-123">Library</span></span><br/> | <dl> <span data-ttu-id="1ba79-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ba79-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1ba79-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ba79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba79-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1ba79-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
