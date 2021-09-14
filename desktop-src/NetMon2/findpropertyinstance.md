---
description: La fonction FindPropertyInstance recherche la première instance de la propriété spécifiée par le paramètre hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: FindPropertyInstance, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110374"
---
# <a name="findpropertyinstance-function"></a>FindPropertyInstance fonction)

La fonction **FindPropertyInstance** recherche la première instance de la propriété spécifiée par le paramètre *hProperty* .

## <a name="syntax"></a>Syntaxe


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame. Le descripteur de frame peut être récupéré par un appel à la fonction [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ dans\]
</dt> <dd>

Handle vers la propriété que vous souhaitez rechercher. Le descripteur de propriété peut être récupéré par un appel à la fonction [GetProperty](getproperty.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit (autrement dit, si la propriété est trouvée), la valeur de retour est un pointeur vers la première instance de la propriété.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Pour récupérer l’instance suivante de la propriété, appelez [FindPropertyInstanceRestart](findpropertyinstancerestart.md).

Les [*experts*](e.md) et les [*analyseurs*](p.md)peuvent appeler la fonction **FindPropertyInstance** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




