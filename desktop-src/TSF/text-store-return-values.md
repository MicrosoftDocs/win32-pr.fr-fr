---
title: Valeurs de retour du magasin de texte (Textstor. h)
description: Lorsqu’un gestionnaire de documents traite un magasin de texte, il génère des valeurs de retour dans la plage comprise entre 0xHHHH0200 et 0xHHHH0300. Le tableau suivant répertorie les valeurs de retour du magasin de texte par ordre alphabétique.
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008808"
---
# <a name="text-store-return-values"></a>Valeurs de retour du magasin de texte

Lorsqu’un gestionnaire de documents traite un magasin de texte, il produit des valeurs de retour dans la plage de 0x *hhhh* 0200 à 0x *hhhh* 0300. Le tableau suivant répertorie les valeurs de retour du magasin de texte par ordre alphabétique.



| Code/valeur de retour                                                                                                                                                                                                                          | Description                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**TS \_ \_Format E**</dt> <dt>0x8004020a</dt> </dl>                   | L’application ne prend pas en charge le type de données contenu dans l’objet [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) à insérer à l’aide de [**ITextStoreACP :: InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded).<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**TS \_ \_INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl> | Le paramètre ne se trouve pas dans le cadre englobant d’un caractère.<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**TS \_ \_INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>       | La plage spécifiée s’étend à l’extérieur du document.<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**TS \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>    | L’objet ne prend pas en charge l’interface demandée.<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**TS \_ E \_ nodisposition**</dt> <dt>0x80040206</dt> </dl>             | L’application n’a pas calculé la disposition du texte.<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**TS \_ 0x80040201 E \_ NOlock**</dt> <dt></dt> </dl>                   | L’application ne dispose pas d’un verrou en lecture seule ou d’un verrou en lecture/écriture pour le document.<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**TS \_ E \_ noobject**</dt> <dt>0x80040202</dt> </dl>             | Le décalage du contenu incorporé n’est pas positionné avant un \_ \_ caractère incorporé TF char.<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**TS \_ E \_ noselect**</dt> <dt>0x80040205</dt> </dl>    | Le document n’a pas de sélection.<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**TS \_ E \_ noservice**</dt> <dt>0x80040203</dt> </dl>          | Impossible de retourner le contenu pour qu’il corresponde au GUID du service.<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**TS \_ E \_ ReadOnly**</dt> <dt>0x80040209</dt> </dl>             | Le document est en lecture seule. Impossible de modifier le contenu.<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**TS \_ 0x00040300 \_ synchrone E**</dt> <dt></dt> </dl>    | Le document ne peut pas être verrouillé de façon synchrone.<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**TS \_ S \_ Async**</dt> <dt>(0x1)</dt> </dl>                         | Le document a reçu un verrou asynchrone.<br/>                                                                                                                                              |



 

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

[**ITextStoreACP :: InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

