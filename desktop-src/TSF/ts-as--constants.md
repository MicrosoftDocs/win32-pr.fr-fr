---
title: Constantes TS_AS_ (Textstor. h)
description: Les indicateurs suivants spécifient les événements qui appellent les méthodes AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511168"
---
# <a name="ts_as_-constants"></a>TS \_ en tant que \_ \* constantes

Les indicateurs suivants spécifient les événements qui appellent les méthodes **AdviseSink** .



| Constante/valeur                                                                                                                                                                                                                                                                                                                                         | Description                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_ En tant que \_ texte \_ modifié**</dt> <dt>(0x1)</dt> </dl>                                                                                                               | Le texte est modifié dans le document.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_ AS \_ sel \_ change**</dt> <dt>(0X2)</dt> </dl>                                                                                                                  | Le texte est sélectionné dans le document.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_ En tant que \_ \_ modification**</dt> de la disposition <dt>(0x4)</dt> </dl>                                                                                                         | La mise en page du document est modifiée.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ En tant que \_ \_ modification d’attr**</dt> <dt>(0x8)</dt> </dl>                                                                                                               | Les attributs du document sont modifiés.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_ En tant que \_ \_ changement d’État**</dt> <dt>(0x10)</dt> </dl>                                                                                                        | L’état du document est modifié.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_ COMME \_ tous les \_ récepteurs**</dt> <dt>(TS \_ As \_ Text \_ change \| TS \_ As \_ sel change TS comme la modification de la \_ \| \_ \_ disposition \_ \| TS \_ comme \_ attr \_ change TS en \| \_ tant que \_ changement d’état \_ )</dt> </dl> | L’un des quatre événements précédents s’est produit dans le document.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





