---
description: La fonction PdhVbIsGoodStatus teste une valeur d’État pour déterminer s’il s’agit d’un code de réussite ou d’échec. Si la valeur d’État est une valeur réussie, la valeur de retour est différente de zéro. S’il s’agit d’un code d’état d’échec, la valeur de retour est égale à zéro.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519115"
---
# <a name="pdhvbisgoodstatus-function"></a>PdhVbIsGoodStatus fonction)

La fonction **PdhVbIsGoodStatus** teste une valeur d’État pour déterminer s’il s’agit d’un code de réussite ou d’échec. Si la valeur d’État est une valeur réussie, la valeur de retour est différente de zéro. S’il s’agit d’un code d’état d’échec, la valeur de retour est égale à zéro.

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbIsGoodStatus ( \_ ByVal StatusValue As long \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*StatusValue* 
</dt> <dd>

Valeur d’État retournée par une autre fonction PDH qui doit être testée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne zéro si le code d’État est un code d’état d’échec. Elle retourne une valeur différente de zéro si le code d’État est un code d’état de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




