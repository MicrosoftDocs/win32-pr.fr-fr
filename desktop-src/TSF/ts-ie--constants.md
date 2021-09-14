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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008785"
---
# <a name="ts_ie_-constants"></a>\_ \_ \* Constantes TS IE

Les \_ \_ \* constantes TS IE décrivent comment insérer du texte qui peut contenir des objets incorporés utilisés par des services de texte.



| Constante/valeur                                                                                                                                                                                                                          | Description                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <dt>**TS \_ \_Correction IE**</dt> <dt>(0x1)</dt> </dl>    | Le texte est une transformation (correction) du contenu existant, et toutes les informations de balisage de texte spéciales (métadonnées) sont conservées, telles que les données de fichier. wav ou un identificateur de langue.<br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <dt>**TS \_ \_Composition IE**</dt> <dt>(0X2)</dt> </dl> | Non utilisé.<br/>                                                                                                                                                                  |



## <a name="remarks"></a>Notes

Ces constantes sont utilisées dans le paramètre *dwFlags* de [ITextStoreACP :: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) et [ITextStoreAnchor :: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITextStoreACP :: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





