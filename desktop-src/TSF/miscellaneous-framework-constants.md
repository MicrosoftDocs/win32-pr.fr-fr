---
title: Constantes d’infrastructure diverses (msctf. h)
description: Les constantes d’infrastructure diverses indiquent des paramètres pour les clients, les processus ou le texte.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466446"
---
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="d8419-103">Constantes d’infrastructure diverses</span><span class="sxs-lookup"><span data-stu-id="d8419-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="d8419-104">Les constantes d’infrastructure diverses indiquent des paramètres pour les clients, les processus ou le texte.</span><span class="sxs-lookup"><span data-stu-id="d8419-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="d8419-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="d8419-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="d8419-106">Description</span><span class="sxs-lookup"><span data-stu-id="d8419-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="d8419-107"><dt>**Tf \_ CLIENTID \_ null**</dt> <dt>((TfClientId) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="d8419-108">Indique à un service de texte que le client est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d8419-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="d8419-109">Consultez [TfClientId](tfclientid.md).</span><span class="sxs-lookup"><span data-stu-id="d8419-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="d8419-110"><dt>**Tf \_ \_GUIDATOM non valide**</dt> <dt>((TfGuidAtom) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="d8419-111">La valeur [TfGuidAtom](tfguidatom.md) du processus en cours n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d8419-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="d8419-112"><dt>**Tf \_ \_sélection par défaut**</dt> <dt>( \_ \_ sélection par défaut des services Terminal Server)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="d8419-113">Utilisez la sélection par défaut.</span><span class="sxs-lookup"><span data-stu-id="d8419-113">Use the default selection.</span></span> <span data-ttu-id="d8419-114">Utilisé par [ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)et [ITextStoreAnchor :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span><span class="sxs-lookup"><span data-stu-id="d8419-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="d8419-115"><dt>**Tf \_ GTP y \_ compris le \_ texte**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="d8419-116">Spécifie que la méthode [ITfEditRecord :: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obtiendra la collection d’objets Range qui couvrent le texte modifié pendant la session d’édition.</span><span class="sxs-lookup"><span data-stu-id="d8419-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="d8419-117"><dt>**Tf \_ \_Objet HF**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="d8419-118">Le décalage de plage s’arrête si un objet incorporé est rencontré.</span><span class="sxs-lookup"><span data-stu-id="d8419-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="d8419-119">Utilisé dans le membre **dwFlags** de la structure [tf \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .</span><span class="sxs-lookup"><span data-stu-id="d8419-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="d8419-120"><dt>**Tf \_ \_Correction IE**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="d8419-121">Le texte est une transformation (correction) du contenu existant, afin que d’autres services de texte puissent conserver les données associées au texte d’origine.</span><span class="sxs-lookup"><span data-stu-id="d8419-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="d8419-122">Utilisé dans le paramètre *dwFlags* de [ITfRange :: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="d8419-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="d8419-123"><dt>**Tf \_ \_Cookie non valide**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="d8419-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d8419-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="d8419-125"><dt>**Tf \_ \_ \_ Cookie d’édition non valide**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="d8419-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d8419-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="d8419-127"><dt>**Tf \_ POPF \_ tout**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="d8419-128">Tous les contextes sont supprimés de la pile.</span><span class="sxs-lookup"><span data-stu-id="d8419-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="d8419-129">Utilisé dans le paramètre *dwFlags* de [ITfDocumentMgr ::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span><span class="sxs-lookup"><span data-stu-id="d8419-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="d8419-130"><dt>**Tf \_ \_Correction St**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="d8419-131">Le texte est une transformation (correction) du contenu existant, afin que d’autres services de texte puissent conserver les données associées au texte d’origine.</span><span class="sxs-lookup"><span data-stu-id="d8419-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="d8419-132">Utilisé dans le paramètre *dwFlags* de [ITfRange :: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span><span class="sxs-lookup"><span data-stu-id="d8419-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="d8419-133"><dt>**Tf \_ \_Correction de ma**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="d8419-134">La modification du texte est le résultat d’une transformation (correction) du contenu existant.</span><span class="sxs-lookup"><span data-stu-id="d8419-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="d8419-135">Cela implique que la sémantique du texte n’a pas changé.</span><span class="sxs-lookup"><span data-stu-id="d8419-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="d8419-136">Utilisé dans le paramètre *dwFlags* de [ITfPropertyStore :: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span><span class="sxs-lookup"><span data-stu-id="d8419-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="d8419-137"><dt>**Tf \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="d8419-138">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d8419-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="d8419-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8419-139">Requirements</span></span>



| <span data-ttu-id="d8419-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8419-140">Requirement</span></span> | <span data-ttu-id="d8419-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8419-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d8419-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8419-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d8419-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8419-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d8419-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8419-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d8419-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8419-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d8419-146">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d8419-146">Redistributable</span></span><br/>          | <span data-ttu-id="d8419-147">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="d8419-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="d8419-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8419-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8419-149"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8419-150">MIDL</span><span class="sxs-lookup"><span data-stu-id="d8419-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8419-151"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8419-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8419-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8419-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8419-153">ITextStoreACP :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="d8419-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="d8419-154">ITextStoreAnchor :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="d8419-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="d8419-155">ITfContext :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="d8419-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="d8419-156">ITfDocumentMgr ::P op</span><span class="sxs-lookup"><span data-stu-id="d8419-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="d8419-157">ITfEditRecord::GetTextAndPropertyUpdates</span><span class="sxs-lookup"><span data-stu-id="d8419-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="d8419-158">ITfPropertyStore::OnTextUpdated</span><span class="sxs-lookup"><span data-stu-id="d8419-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="d8419-159">ITfRange::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="d8419-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="d8419-160">ITfRange :: SetText</span><span class="sxs-lookup"><span data-stu-id="d8419-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="d8419-161">TfClientId</span><span class="sxs-lookup"><span data-stu-id="d8419-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="d8419-162">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="d8419-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="d8419-163">TF \_ HALTCOND</span><span class="sxs-lookup"><span data-stu-id="d8419-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





