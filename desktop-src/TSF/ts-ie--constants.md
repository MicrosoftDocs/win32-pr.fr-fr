---
title: Constantes TS_IE_ (Textstor. h)
description: Les \_ \_ constantes TS IE \ décrivent comment insérer du texte qui peut contenir des objets incorporés utilisés par des services de texte.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103281"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="c0677-103">\_ \_ \* Constantes TS IE</span><span class="sxs-lookup"><span data-stu-id="c0677-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="c0677-104">Les \_ \_ \* constantes TS IE décrivent comment insérer du texte qui peut contenir des objets incorporés utilisés par des services de texte.</span><span class="sxs-lookup"><span data-stu-id="c0677-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="c0677-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="c0677-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="c0677-106">Description</span><span class="sxs-lookup"><span data-stu-id="c0677-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="c0677-107"><dt>**TS \_ \_Correction IE**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c0677-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="c0677-108">Le texte est une transformation (correction) du contenu existant, et toutes les informations de balisage de texte spéciales (métadonnées) sont conservées, telles que les données de fichier. wav ou un identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="c0677-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="c0677-109"><dt>**TS \_ \_Composition IE**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="c0677-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="c0677-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c0677-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="c0677-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c0677-111">Remarks</span></span>

<span data-ttu-id="c0677-112">Ces constantes sont utilisées dans le paramètre *dwFlags* de [ITextStoreACP :: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) et [ITextStoreAnchor :: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="c0677-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0677-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0677-113">Requirements</span></span>



| <span data-ttu-id="c0677-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0677-114">Requirement</span></span> | <span data-ttu-id="c0677-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0677-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0677-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0677-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0677-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0677-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0677-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0677-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0677-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0677-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0677-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c0677-120">Redistributable</span></span><br/>          | <span data-ttu-id="c0677-121">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="c0677-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="c0677-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0677-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0677-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0677-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0677-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="c0677-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0677-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0677-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0677-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0677-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0677-127">ITextStoreACP :: InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="c0677-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="c0677-128">ITextStoreAnchor::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="c0677-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





