---
description: 'Énumération D3DX10_ERR : les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.'
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: Énumération D3DX10_ERR (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094351"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="2ee9c-103">D3DX10 \_ Err (énumération)</span><span class="sxs-lookup"><span data-stu-id="2ee9c-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="2ee9c-104">Les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="2ee9c-105">La liste suivante répertorie les valeurs qui peuvent être retournées par les méthodes incluses dans la bibliothèque de l’utilitaire D3DX.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="2ee9c-106">Consultez les descriptions des méthodes individuelles pour obtenir la liste des valeurs que chaque peut retourner.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="2ee9c-107">Ces listes ne sont pas nécessairement exhaustives.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee9c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ee9c-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="2ee9c-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="2ee9c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2ee9c-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ Err \_ ne peut pas \_ modifier le \_ tampon d’index \_**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-111">Le tampon d’index ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10 \_ erreur \_ de \_ maillage non valide**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-113">Le maillage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**L' \_ erreur d3dx10 \_ ne peut pas être \_ \_ triée**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-115">L’attribut sort (D3DXMESHOPT \_ ATTRSORT) n’est pas pris en charge en tant que technique d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10 \_ Err de l’erreur \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-117">L’apparence n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ Err \_ trop \_ grand \_**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-119">Trop d’influences spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10 \_ des \_ données non valides \_**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-121">Les données ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**La \_ \_ maille chargée d3dx10 Err \_ \_ \_ n’a pas de \_ données**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-123">La maille n’a pas de données.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ Err \_ dupliquer le \_ \_ fragment nommé**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-125">Un fragment portant ce nom existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9c-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ Err \_ ne peut pas \_ supprimer le \_ dernier \_ élément**</span><span class="sxs-lookup"><span data-stu-id="2ee9c-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="2ee9c-127">Impossible de supprimer le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ee9c-128">Notes </span><span class="sxs-lookup"><span data-stu-id="2ee9c-128">Remarks</span></span>

<span data-ttu-id="2ee9c-129">Le code \_ d’installation FACDD est utilisé pour générer des codes d’erreur, comme dans les macros suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="2ee9c-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ee9c-130">Requirements</span></span>



| <span data-ttu-id="2ee9c-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ee9c-131">Requirement</span></span> | <span data-ttu-id="2ee9c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ee9c-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee9c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ee9c-133">Header</span></span><br/> | <dl> <span data-ttu-id="2ee9c-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9c-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee9c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ee9c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee9c-136">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="2ee9c-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




