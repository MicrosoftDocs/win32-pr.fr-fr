---
title: Constantes TS_IAS_ (Textstor. h)
description: Les \_ \_ constantes TS IAS \ sont utilisées comme indicateurs de champ de bits pour contrôler l’insertion de texte ou d’objets incorporés au niveau d’une sélection ou d’un point d’insertion.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008784"
---
# <a name="ts_ias_-constants"></a>\_ \_ \* CONSTANTEs IAS TS

Les \_ constantes d’IAS TS \_ \* sont utilisées en tant qu’indicateurs de champ de champ pour contrôler l’insertion de texte ou d’objets incorporés au niveau d’une sélection ou d’un point d’insertion.



| Constante/valeur                                                                                                                                                                                                                       | Description                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**TS \_ \_NOQUERY IAS**</dt> <dt>(0x1)</dt> </dl>       | Le texte est inséré et le pointeur de plage a la valeur **null** lors de la fermeture. Ne peut pas être combiné avec l' \_ indicateur QUERYONLY de l’IAS TS \_ .<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**TS \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt> </dl> | N’effectuez pas l’insertion. L’appelant requiert la définition du pointeur de plage. Ne peut pas être combiné avec \_ l' \_ indicateur noquery IAS TS.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





