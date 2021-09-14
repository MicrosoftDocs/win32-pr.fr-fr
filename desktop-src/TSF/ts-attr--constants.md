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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008794"
---
# <a name="ts_attr_-constants"></a>\_Constantes de l’attr TS \_ \*

Les \_ \_ \* constantes d’attribut d’attribut TS sont utilisées pour obtenir et modifier les valeurs des attributs de document. Ces constantes constituent les valeurs possibles des indicateurs de champ de champ dans les méthodes [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) et [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .



| Constante/valeur                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ ATTR \_ Rechercher \_ vers l’arrière**</dt> <dt>(0x1)</dt> </dl>        | Rechercher vers le haut à partir du caractère de début ou de la position d’ancrage pour la position où une transition se produit dans une valeur d’attribut de document. La valeur par défaut est Rechercher vers l’avant.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ \_ \_ \_ Décalage**</dt> de la recherche de l’attr <dt>(0X2)</dt> </dl> | Retourne le nombre de caractères entre le caractère de début ou la position d’ancrage (**acpStart** dans [ITextStoreACP :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) ou **PaStart** dans [ITextStoreAnchor :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) et la position à laquelle une transition d’attribut se produit.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ ATTR \_ Find \_ UPDATESTART**</dt> <dt>(0x4)</dt> </dl>  | Utilisé par [ITextStoreAnchor :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) pour positionner l’ancre d’entrée lors de la transition d’attribut suivante, le cas échéant. Dans le cas contraire, l’ancre d’entrée n’est pas modifiée.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ \_ \_ \_ Valeur souhaitée de la recherche attr**</dt> <dt>(0x8)</dt> </dl>    | Chargez les valeurs d’attribut de document prises en charge dans la structure [ \_ ATTRVAL TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ Fin de l’ATTR \_ Find \_ souhaitée \_**</dt> <dt>(0x10)</dt> </dl>         | Utilisé par [ITextStoreACP :: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) et [ITextStoreAnchor :: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) pour obtenir les valeurs d’attribut de document qui se terminent au caractère ou à la position d’ancrage spécifiés.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ \_Attribut de recherche \_ masqué**</dt> <dt>(0x20)</dt> </dl>                | Réservé.<br/>                                                                                                                                                                                                                                                                                                                                               |



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

[\_ATTRID TS](ts-attrid.md)
</dt> <dt>

[\_ATTRVAL TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP :: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP :: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





