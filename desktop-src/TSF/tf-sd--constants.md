---
title: Constantes TF_SD_ (msctf. h)
description: Les \_ \_ constantes TF SD \ décrivent l’état du document.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103013"
---
# <a name="tf_sd_-constants"></a>\_ \_ \* Constantes TF SD

Les \_ \_ \* constantes TF SD décrivent l’état du document.



| Constante/valeur                                                                                                                                                                                                                              | Description                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**Tf \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt> </dl> | Le document est en lecture seule et ne peut pas être modifié.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**Tf \_ \_chargement SD**</dt> <dt>( \_ chargement SD TS \_ )</dt> </dl>     | Le document est en cours de chargement et peut être incomplet.<br/>    |



## <a name="remarks"></a>Notes

Le membre **dwDynamicFlags** de la structure d' [ \_ État TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) utilise ces constantes.

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

[\_État TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[\_ \_ \* Constantes TS DP](ts-sd--constants.md)
</dt> <dt>

[ITfContextOwner :: GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITfContextOwnerServices :: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP :: GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITfStatusSunk :: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

