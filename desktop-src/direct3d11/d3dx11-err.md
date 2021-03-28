---
title: Énumération D3DX11_ERR (D3DX11. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.'
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- Énumération D3DX11_ERR Direct3D 11
- Pointeur d’énumération LPD3DX11_ERR Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996200"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="16c86-106">D3DX11 \_ Err (énumération)</span><span class="sxs-lookup"><span data-stu-id="16c86-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="16c86-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="16c86-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="16c86-108">Les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.</span><span class="sxs-lookup"><span data-stu-id="16c86-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="16c86-109">La liste suivante répertorie les valeurs qui peuvent être retournées par les méthodes incluses dans la bibliothèque de l’utilitaire D3DX.</span><span class="sxs-lookup"><span data-stu-id="16c86-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="16c86-110">Consultez les descriptions des méthodes individuelles pour obtenir la liste des valeurs que chaque peut retourner.</span><span class="sxs-lookup"><span data-stu-id="16c86-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="16c86-111">Ces listes ne sont pas nécessairement exhaustives.</span><span class="sxs-lookup"><span data-stu-id="16c86-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c86-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16c86-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="16c86-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="16c86-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="16c86-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ ne peut pas \_ modifier le \_ tampon d’index \_**</span><span class="sxs-lookup"><span data-stu-id="16c86-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-115">Le tampon d’index ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="16c86-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ erreur \_ de \_ maillage non valide**</span><span class="sxs-lookup"><span data-stu-id="16c86-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-117">Le maillage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="16c86-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**L' \_ erreur D3DX11 \_ ne peut pas être \_ \_ triée**</span><span class="sxs-lookup"><span data-stu-id="16c86-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-119">L’attribut sort (D3DXMESHOPT \_ ATTRSORT) n’est pas pris en charge en tant que technique d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="16c86-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11 \_ Err de l’erreur \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="16c86-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-121">L’apparence n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="16c86-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ Err \_ trop \_ grand \_**</span><span class="sxs-lookup"><span data-stu-id="16c86-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-123">Trop d’influences spécifiées.</span><span class="sxs-lookup"><span data-stu-id="16c86-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ des \_ données non valides \_**</span><span class="sxs-lookup"><span data-stu-id="16c86-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-125">Les données ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="16c86-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**La \_ \_ maille chargée D3DX11 Err \_ \_ \_ n’a pas de \_ données**</span><span class="sxs-lookup"><span data-stu-id="16c86-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-127">La maille n’a pas de données.</span><span class="sxs-lookup"><span data-stu-id="16c86-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ Err \_ dupliquer le \_ \_ fragment nommé**</span><span class="sxs-lookup"><span data-stu-id="16c86-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-129">Un fragment portant ce nom existe déjà.</span><span class="sxs-lookup"><span data-stu-id="16c86-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="16c86-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ ne peut pas \_ supprimer le \_ dernier \_ élément**</span><span class="sxs-lookup"><span data-stu-id="16c86-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="16c86-131">Impossible de supprimer le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="16c86-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16c86-132">Notes</span><span class="sxs-lookup"><span data-stu-id="16c86-132">Remarks</span></span>

<span data-ttu-id="16c86-133">Le code \_ d’installation FACDD est utilisé pour générer des codes d’erreur, comme dans les macros suivantes.</span><span class="sxs-lookup"><span data-stu-id="16c86-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="16c86-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16c86-134">Requirements</span></span>



| <span data-ttu-id="16c86-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16c86-135">Requirement</span></span> | <span data-ttu-id="16c86-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="16c86-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16c86-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="16c86-137">Header</span></span><br/> | <dl> <span data-ttu-id="16c86-138"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="16c86-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c86-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16c86-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c86-140">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="16c86-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





