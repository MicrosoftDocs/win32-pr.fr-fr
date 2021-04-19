---
title: Constantes TF_IAS_ (msctf. h)
description: Les \_ \_ constantes TF IAS \ sont utilisées comme indicateurs de champ de bits dans les méthodes qui insèrent du texte ou des objets incorporés au niveau d’une sélection ou d’un point d’insertion.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512387"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="193b8-103">\_ \_ \* CONSTANTEs IAS TF</span><span class="sxs-lookup"><span data-stu-id="193b8-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="193b8-104">Les \_ \_ \* constantes IAS TF sont utilisées en tant qu’indicateurs de champ de champ dans les méthodes qui insèrent du texte ou des objets incorporés au niveau d’une sélection ou d’un point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="193b8-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="193b8-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="193b8-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="193b8-106">Description</span><span class="sxs-lookup"><span data-stu-id="193b8-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="193b8-107"><dt>**Tf \_ \_NOQUERY IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="193b8-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="193b8-108">Le texte est inséré et le pointeur de plage a la valeur **null** lors de la fermeture.</span><span class="sxs-lookup"><span data-stu-id="193b8-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="193b8-109">Ne peut pas être combiné avec \_ l' \_ indicateur QUERYONLY IAS TF.</span><span class="sxs-lookup"><span data-stu-id="193b8-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="193b8-110"><dt>**Tf \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="193b8-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="193b8-111">N’effectuez pas l’insertion.</span><span class="sxs-lookup"><span data-stu-id="193b8-111">Do not perform the insert.</span></span> <span data-ttu-id="193b8-112">L’appelant requiert la définition du pointeur de plage.</span><span class="sxs-lookup"><span data-stu-id="193b8-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="193b8-113">Ne peut pas être combiné avec \_ l' \_ indicateur de requête IAS TF.</span><span class="sxs-lookup"><span data-stu-id="193b8-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="193b8-114"><dt>**Tf \_ IAS \_ sans \_ \_ composition par défaut**</dt> <dt>(0x80000000)</dt></span><span class="sxs-lookup"><span data-stu-id="193b8-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="193b8-115">TSF ne crée pas de composition par défaut si une composition est requise.</span><span class="sxs-lookup"><span data-stu-id="193b8-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="193b8-116">L’appelant doit démarrer une composition sur la plage.</span><span class="sxs-lookup"><span data-stu-id="193b8-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="193b8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="193b8-117">Requirements</span></span>



| <span data-ttu-id="193b8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="193b8-118">Requirement</span></span> | <span data-ttu-id="193b8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="193b8-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="193b8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="193b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="193b8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="193b8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="193b8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="193b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="193b8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="193b8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="193b8-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="193b8-124">Redistributable</span></span><br/>          | <span data-ttu-id="193b8-125">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="193b8-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="193b8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="193b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="193b8-127"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="193b8-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="193b8-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="193b8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="193b8-129"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="193b8-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="193b8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="193b8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193b8-131">ITextStoreACP :: InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="193b8-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="193b8-132">ITextStoreACP :: InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="193b8-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="193b8-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="193b8-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="193b8-134">ITextStoreAnchor::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="193b8-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="193b8-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="193b8-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="193b8-136">ITfInsertAtSelection::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="193b8-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





