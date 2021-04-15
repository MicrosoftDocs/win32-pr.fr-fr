---
title: Constantes TS_ATTR_ (Textstor. h)
description: Les \_ \_ constantes de l’attribut de serveur TS \ constantes sont utilisées pour obtenir et modifier les valeurs des attributs de document. Ces constantes constituent les valeurs possibles des indicateurs de champ de champ dans les méthodes ITextStoreACP et ITextStoreAnchor.
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466162"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="f7157-104">\_Constantes de l’attr TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="f7157-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="f7157-105">Les \_ \_ \* constantes d’attribut d’attribut TS sont utilisées pour obtenir et modifier les valeurs des attributs de document.</span><span class="sxs-lookup"><span data-stu-id="f7157-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="f7157-106">Ces constantes constituent les valeurs possibles des indicateurs de champ de champ dans les méthodes [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) et [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="f7157-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="f7157-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="f7157-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="f7157-108">Description</span><span class="sxs-lookup"><span data-stu-id="f7157-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="f7157-109"><dt>**TS \_ ATTR \_ Rechercher \_ vers l’arrière**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="f7157-110">Rechercher vers le haut à partir du caractère de début ou de la position d’ancrage pour la position où une transition se produit dans une valeur d’attribut de document.</span><span class="sxs-lookup"><span data-stu-id="f7157-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="f7157-111">La valeur par défaut est Rechercher vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="f7157-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="f7157-112"><dt>**TS \_ \_ \_ \_ Décalage**</dt> de la recherche de l’attr <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="f7157-113">Retourne le nombre de caractères entre le caractère de début ou la position d’ancrage (**acpStart** dans [ITextStoreACP :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) ou **PaStart** dans [ITextStoreAnchor :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) et la position à laquelle une transition d’attribut se produit.</span><span class="sxs-lookup"><span data-stu-id="f7157-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="f7157-114"><dt>**TS \_ ATTR \_ Find \_ UPDATESTART**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="f7157-115">Utilisé par [ITextStoreAnchor :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) pour positionner l’ancre d’entrée lors de la transition d’attribut suivante, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f7157-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="f7157-116">Dans le cas contraire, l’ancre d’entrée n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="f7157-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="f7157-117"><dt>**TS \_ \_ \_ \_ Valeur souhaitée de la recherche attr**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="f7157-118">Chargez les valeurs d’attribut de document prises en charge dans la structure [ \_ ATTRVAL TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .</span><span class="sxs-lookup"><span data-stu-id="f7157-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="f7157-119"><dt>**TS \_ Fin de l’ATTR \_ Find \_ souhaitée \_**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="f7157-120">Utilisé par [ITextStoreACP :: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) et [ITextStoreAnchor :: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) pour obtenir les valeurs d’attribut de document qui se terminent au caractère ou à la position d’ancrage spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f7157-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="f7157-121"><dt>**TS \_ \_Attribut de recherche \_ masqué**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="f7157-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f7157-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="f7157-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7157-123">Requirements</span></span>



| <span data-ttu-id="f7157-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7157-124">Requirement</span></span> | <span data-ttu-id="f7157-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7157-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7157-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7157-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f7157-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7157-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f7157-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7157-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f7157-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7157-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7157-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f7157-130">Redistributable</span></span><br/>          | <span data-ttu-id="f7157-131">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="f7157-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="f7157-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7157-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7157-133"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7157-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="f7157-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7157-135"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7157-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7157-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7157-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7157-137">\_ATTRID TS</span><span class="sxs-lookup"><span data-stu-id="f7157-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="f7157-138">\_ATTRVAL TS</span><span class="sxs-lookup"><span data-stu-id="f7157-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="f7157-139">ITextStoreACP :: FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="f7157-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="f7157-140">ITextStoreACP :: RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="f7157-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="f7157-141">ITextStoreAnchor::FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="f7157-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="f7157-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="f7157-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





