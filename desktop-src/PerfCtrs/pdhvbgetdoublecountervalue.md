---
description: La fonction PdhVbGetDoubleCounterValue retourne la valeur actuelle du compteur spécifié sous la forme d’une valeur à virgule flottante double précision.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416657"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>PdhVbGetDoubleCounterValue fonction)

La fonction **PdhVbGetDoubleCounterValue** retourne la valeur actuelle du compteur spécifié sous la forme d’une valeur à virgule flottante double précision. Vous devez vérifier *CounterStatus* avant d’utiliser le nombre retourné, car le compteur peut ne pas être valide lorsqu’il est lu. Pour vérifier l’état du compteur, appelez la fonction [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbGetDoubleCounterValue ( \_ ByVal CounterHandle As long, \_ ByVal CounterStatus As long \_ ) As Double

## <a name="parameters"></a>Paramètres

<dl> <dt>

*CounterHandle* 
</dt> <dd>

ID du compteur dont la valeur actuelle doit être lue.

</dd> <dt>

*CounterStatus* 
</dt> <dd>

Variable dans laquelle l’état actuel de la valeur de compteur est retourné à l’appelant. La valeur de données renvoyée est valide si et seulement si la valeur retournée dans CounterStatus est PDH \_ CSTATUS \_ Valid \_ Data ou PDH \_ CSTATUS \_ New \_ Data (voir les codes d’erreur PDH). Si la valeur retournée dans CounterStatus est toute autre valeur, n’utilisez pas les données.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La fonction retourne la valeur à virgule flottante double précision du compteur actuel, calculée et mise en forme comme défini par le type de compteur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




