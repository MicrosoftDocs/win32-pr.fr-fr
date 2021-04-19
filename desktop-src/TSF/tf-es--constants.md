---
title: Constantes TF_ES_ (msctf. h)
description: Les constantes suivantes sont utilisées par la méthode ITfContext RequestEditSession.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509548"
---
# <a name="tf_es_-constants"></a>\_ \_ \* Constantes TF es

Les constantes suivantes sont utilisées par la méthode [ITfContext :: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .



| Constante/valeur                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**Tf \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt> </dl> | La session d’édition peut se produire de façon synchrone ou asynchrone, à la discrétion du responsable. Le gestionnaire va tenter de planifier une session d’édition synchrone pour améliorer les performances. Cette valeur ne peut pas être combinée avec les \_ valeurs de synchronisation TF es \_ Async ou TF \_ es \_ .<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**Tf \_ \_Synchronisation es**</dt> <dt>(0x1)</dt> </dl>                          | La session d’édition doit être synchrone ou la demande échoue (avec TF \_ E \_ Synchronous). Cet indicateur doit être utilisé uniquement dans les situations documentées (telles que la gestion des séquences de touches) où il peut être attendu. Dans le cas contraire, l’appel échouera probablement. Cette valeur ne peut pas être combinée avec \_ les \_ valeurs ASYNCDONTCARE TF es ou TF \_ es \_ Async.<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**Tf \_ ES \_ lus**</dt> <dt>(0X2)</dt> </dl>                          | Demande l’accès en lecture seule au contexte.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**Tf \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl>           | Demande l’accès en lecture/écriture au contexte.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt> </dl>                       | La session d’édition doit être asynchrone ou la demande échouera. Cette valeur ne peut pas être combinée avec les \_ valeurs de synchronisation TF es \_ ASYNCDONTCARE ou TF \_ es \_ .<br/>                                                                                                                                                                                         |



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

[ITfContext :: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





