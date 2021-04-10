---
title: Constantes de magasin de texte diverses (Textstor. h)
description: Les constantes du magasin de texte divers définissent certaines propriétés pour les magasins de texte.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105400"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="2a43d-103">Constantes de magasin de texte diverses</span><span class="sxs-lookup"><span data-stu-id="2a43d-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="2a43d-104">Les constantes du magasin de texte divers définissent certaines propriétés pour les magasins de texte.</span><span class="sxs-lookup"><span data-stu-id="2a43d-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="2a43d-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="2a43d-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="2a43d-106">Description</span><span class="sxs-lookup"><span data-stu-id="2a43d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="2a43d-107"><dt>**TS \_ \_Sélection par défaut**</dt> <dt>((ULONG)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="2a43d-108">Si le paramètre *ulIndex* de [ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) est défini sur cette valeur, la sélection par défaut est obtenue.</span><span class="sxs-lookup"><span data-stu-id="2a43d-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="2a43d-109"><dt>**TS \_ GEA \_ masqué**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="2a43d-110">Si le paramètre *dwFlags* de [ITextStoreAnchor :: GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) est défini sur cette valeur, un objet incorporé peut être localisé dans le texte masqué.</span><span class="sxs-lookup"><span data-stu-id="2a43d-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="2a43d-111"><dt>**TS \_ GTA \_ masqué**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="2a43d-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a43d-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="2a43d-113"><dt>**TS \_ \_Correction St**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="2a43d-114">Si le paramètre *dwFlags* de [ITextStoreACP :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)ou [ITextStoreACPSink :: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) est défini sur cette valeur, le texte est une transformation (correction) du contenu existant et toutes les informations de balisage de texte spéciales (métadonnées) sont conservées, telles que les données de fichier. wav ou un identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="2a43d-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="2a43d-115"><dt>**TS \_ \_Correction TC**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="2a43d-116">Si le paramètre *dwFlags* de [ITextStoreAnchorSink :: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) est défini sur cette valeur, le texte est une transformation (correction) du contenu existant, et toutes les informations de balisage de texte spéciales (métadonnées) sont conservées, telles que les données de fichier. wav ou un identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="2a43d-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="2a43d-117"><dt>**TS \_ VCOOKIE \_ nul**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="2a43d-118">Utilisé en interne par TSF.</span><span class="sxs-lookup"><span data-stu-id="2a43d-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="2a43d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a43d-119">Requirements</span></span>



| <span data-ttu-id="2a43d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a43d-120">Requirement</span></span> | <span data-ttu-id="2a43d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a43d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a43d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a43d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a43d-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a43d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2a43d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a43d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a43d-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a43d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a43d-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2a43d-126">Redistributable</span></span><br/>          | <span data-ttu-id="2a43d-127">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="2a43d-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="2a43d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a43d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a43d-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a43d-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="2a43d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a43d-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a43d-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a43d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a43d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a43d-133">ITfContext :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="2a43d-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="2a43d-134">ITextStoreACP :: SetText</span><span class="sxs-lookup"><span data-stu-id="2a43d-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="2a43d-135">ITextStoreAnchor :: SetText</span><span class="sxs-lookup"><span data-stu-id="2a43d-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="2a43d-136">ITextStoreAnchor::GetEmbedded</span><span class="sxs-lookup"><span data-stu-id="2a43d-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="2a43d-137">ITextStoreACPSink :: OnTextChange</span><span class="sxs-lookup"><span data-stu-id="2a43d-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="2a43d-138">ITextStoreAnchorSink::OnTextChange</span><span class="sxs-lookup"><span data-stu-id="2a43d-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="2a43d-139">Constantes d’infrastructure diverses</span><span class="sxs-lookup"><span data-stu-id="2a43d-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





