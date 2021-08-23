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
ms.openlocfilehash: f9bcd6ad253e71d662cbc713398e65c6a250863e18a9fe2d461a2d93717fb7b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906009"
---
# <a name="miscellaneous-framework-constants"></a>Constantes d’infrastructure diverses

Les constantes d’infrastructure diverses indiquent des paramètres pour les clients, les processus ou le texte.



| Constante/valeur                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**Tf \_ CLIENTID \_ null**</dt> <dt>((TfClientId) 0)</dt> </dl>                        | Indique à un service de texte que le client est désactivé. Consultez [TfClientId](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**Tf \_ \_GUIDATOM non valide**</dt> <dt>((TfGuidAtom) 0)</dt> </dl>               | La valeur [TfGuidAtom](tfguidatom.md) du processus en cours n’est pas valide.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**Tf \_ \_sélection par défaut**</dt> <dt>( \_ \_ sélection par défaut des services Terminal Server)</dt> </dl> | Utilisez la sélection par défaut. Utilisé par [ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)et [ITextStoreAnchor :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**Tf \_ GTP y \_ compris le \_ texte**</dt> <dt>(0x1)</dt> </dl>                               | Spécifie que la méthode [ITfEditRecord :: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obtiendra la collection d’objets Range qui couvrent le texte modifié pendant la session d’édition.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**Tf \_ \_Objet HF**</dt> <dt>(1)</dt> </dl>                                              | Le décalage de plage s’arrête si un objet incorporé est rencontré. Utilisé dans le membre **dwFlags** de la structure [tf \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**Tf \_ \_Correction IE**</dt> <dt>(1)</dt> </dl>                                  | Le texte est une transformation (correction) du contenu existant, afin que d’autres services de texte puissent conserver les données associées au texte d’origine. Utilisé dans le paramètre *dwFlags* de [ITfRange :: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**Tf \_ \_Cookie non valide**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                      | Non utilisé.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**Tf \_ \_ \_ Cookie d’édition non valide**</dt> <dt>(0)</dt> </dl>               | Non utilisé.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**Tf \_ POPF \_ tout**</dt> <dt>(0x1)</dt> </dl>                                               | Tous les contextes sont supprimés de la pile. Utilisé dans le paramètre *dwFlags* de [ITfDocumentMgr ::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**Tf \_ \_Correction St**</dt> <dt>(1)</dt> </dl>                                  | Le texte est une transformation (correction) du contenu existant, afin que d’autres services de texte puissent conserver les données associées au texte d’origine. Utilisé dans le paramètre *dwFlags* de [ITfRange :: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**Tf \_ \_Correction de ma**</dt> <dt>(0x1)</dt> </dl>                                | La modification du texte est le résultat d’une transformation (correction) du contenu existant. Cela implique que la sémantique du texte n’a pas changé. Utilisé dans le paramètre *dwFlags* de [ITfPropertyStore :: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**Tf \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt> </dl>                                | Non utilisé.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITextStoreACP :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr ::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[ITfRange :: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





