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
# <a name="tf_ias_-constants"></a>\_ \_ \* CONSTANTEs IAS TF

Les \_ \_ \* constantes IAS TF sont utilisées en tant qu’indicateurs de champ de champ dans les méthodes qui insèrent du texte ou des objets incorporés au niveau d’une sélection ou d’un point d’insertion.



| Constante/valeur                                                                                                                                                                                                                                                                       | Description                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <dt>**Tf \_ \_NOQUERY IAS**</dt> <dt>(0x1)</dt> </dl>                                                       | Le texte est inséré et le pointeur de plage a la valeur **null** lors de la fermeture. Ne peut pas être combiné avec \_ l' \_ indicateur QUERYONLY IAS TF.<br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <dt>**Tf \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt> </dl>                                                 | N’effectuez pas l’insertion. L’appelant requiert la définition du pointeur de plage. Ne peut pas être combiné avec \_ l' \_ indicateur de requête IAS TF.<br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <dt>**Tf \_ IAS \_ sans \_ \_ composition par défaut**</dt> <dt>(0x80000000)</dt> </dl> | TSF ne crée pas de composition par défaut si une composition est requise. L’appelant doit démarrer une composition sur la plage.<br/>         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITextStoreACP :: InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[ITextStoreACP :: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[ITextStoreAnchor::InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[ITextStoreAnchor::InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertTextAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





