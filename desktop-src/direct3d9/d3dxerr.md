---
description: Énumération D3DXERR-les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Énumération D3DXERR (D3dx9. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 1c1dd03500a493b30d7c1d3bfdfdf800b65a6d82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094302"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="da4f2-103">Énumération D3DXERR</span><span class="sxs-lookup"><span data-stu-id="da4f2-103">D3DXERR enumeration</span></span>

<span data-ttu-id="da4f2-104">Les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.</span><span class="sxs-lookup"><span data-stu-id="da4f2-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="da4f2-105">La liste suivante répertorie les valeurs qui peuvent être retournées par les méthodes incluses dans la bibliothèque de l’utilitaire D3DX.</span><span class="sxs-lookup"><span data-stu-id="da4f2-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="da4f2-106">Consultez les descriptions des méthodes individuelles pour obtenir la liste des valeurs que chaque peut retourner.</span><span class="sxs-lookup"><span data-stu-id="da4f2-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="da4f2-107">Ces listes ne sont pas nécessairement exhaustives.</span><span class="sxs-lookup"><span data-stu-id="da4f2-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da4f2-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="da4f2-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="da4f2-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da4f2-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="da4f2-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-111">Le tampon d’index ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="da4f2-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**</span><span class="sxs-lookup"><span data-stu-id="da4f2-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-113">Le maillage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="da4f2-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="da4f2-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-115">L’attribut sort (D3DXMESHOPT \_ ATTRSORT) n’est pas pris en charge en tant que technique d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="da4f2-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="da4f2-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-117">L’apparence n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="da4f2-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="da4f2-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-119">Trop d’influences spécifiées.</span><span class="sxs-lookup"><span data-stu-id="da4f2-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ sera déplacé**</span><span class="sxs-lookup"><span data-stu-id="da4f2-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-121">Les données ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="da4f2-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**</span><span class="sxs-lookup"><span data-stu-id="da4f2-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-123">La maille n’a pas de données.</span><span class="sxs-lookup"><span data-stu-id="da4f2-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="da4f2-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-125">Un fragment portant ce nom existe déjà.</span><span class="sxs-lookup"><span data-stu-id="da4f2-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="da4f2-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**</span><span class="sxs-lookup"><span data-stu-id="da4f2-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="da4f2-127">Impossible de supprimer le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="da4f2-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da4f2-128">Notes </span><span class="sxs-lookup"><span data-stu-id="da4f2-128">Remarks</span></span>

<span data-ttu-id="da4f2-129">Le code \_ d’installation FACDD est utilisé pour générer des codes d’erreur, comme dans les macros suivantes.</span><span class="sxs-lookup"><span data-stu-id="da4f2-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="da4f2-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da4f2-130">Requirements</span></span>



| <span data-ttu-id="da4f2-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da4f2-131">Requirement</span></span> | <span data-ttu-id="da4f2-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="da4f2-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da4f2-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="da4f2-133">Header</span></span><br/> | <dl> <span data-ttu-id="da4f2-134"><dt>D3dx9. h</dt></span><span class="sxs-lookup"><span data-stu-id="da4f2-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4f2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da4f2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4f2-136">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="da4f2-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




