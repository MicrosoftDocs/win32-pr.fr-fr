---
description: Le tableau suivant contient les codes d’erreur spécifiques à Microsoft DirectX Media Objects (DMOs). Ces codes d’erreur sont définis dans le fichier d’en-tête Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO Codes d’erreur (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312397"
---
# <a name="dmo-error-codes"></a>DMO Codes d’erreur

Le tableau suivant contient les codes d’erreur spécifiques à Microsoft DirectX Media Objects (DMOs). Ces codes d’erreur sont définis dans le fichier d’en-tête Mediaerr. h.



| Constante/valeur                                                                                                                                                                                                                                                  | Description                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ \_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Index de flux non valide.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ \_INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | Type de média non valide.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ \_Type E \_ non \_ défini**</dt> <dt>0x80040203</dt> </dl>                 | Le type de média n’a pas été défini. Un ou plusieurs flux nécessitent un type de média avant que cette opération puisse être effectuée.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ \_NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | Impossible d’accepter les données sur ce flux. Vous devrez peut-être traiter davantage de données de sortie. consultez [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ \_Type E \_ non \_ accepté**</dt> <dt>0x80040205</dt> </dl>  | Le type de média n’a pas été accepté.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ \_ plus d' \_ éléments**</dt> <dt>0x80040206</dt> </dl>              | L’index de type de média est hors limites.<br/>                                                                                                                        |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mediaerr. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DMO Constantes](dmo-constants.md)
</dt> </dl>

 

 




