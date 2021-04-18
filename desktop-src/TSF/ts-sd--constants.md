---
title: Constantes TS_SD_ (Textstor. h)
description: Les \_ \_ constantes TS SD \ décrivent les États de documents dynamiques utilisés par une application au moment de l’exécution.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512791"
---
# <a name="ts_sd_-constants"></a>\_ \_ \* Constantes TS DP

Les \_ \_ \* constantes TS SD décrivent les États de documents dynamiques utilisés par une application au moment de l’exécution.



| Constante/valeur                                                                                                                                                                                                                                              | Description                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt> </dl>                              | Le document est en lecture seule et ne peut pas être modifié.<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**TS \_ \_Chargement SD**</dt> <dt>(0X2)</dt> </dl>                                 | Le document est en cours de chargement et peut être incomplet.<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**TS \_ SD \_ MASKALL**</dt> (chargement SD TS en <dt> \_ \_ lecture seule TS \| \_ \_ )</dt> </dl> | Le document est à la fois en lecture seule et en cours de chargement.<br/>       |



## <a name="remarks"></a>Notes

Le membre **dwDynamicFlags** de la structure d' [ \_ État TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) utilise ces constantes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_statut TS](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[\_ \_ \* Constantes TF SD](tf-sd--constants.md)
</dt> </dl>

 

 





