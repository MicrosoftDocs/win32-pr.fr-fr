---
description: La méthode GetRange obtient la plage de valeurs valides pour une propriété de qualité d’appel donnée.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'ITCallQualityControl :: GetRange, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d21c9266e64a9bcb31da0028a0ea28b8de98793d56d5bcf28c791c5497756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762435"
---
# <a name="itcallqualitycontrolgetrange-method"></a>ITCallQualityControl :: GetRange, méthode

\[cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetRange** obtient la plage de valeurs valides pour une [propriété de qualité d’appel](callqualityproperty.md)donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Propriété* \[ dans\]
</dt> <dd>

Membre de l’énumération [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*plMin* \[ à\]
</dt> <dd>

Valeur minimale valide pour la propriété d’entrée.

</dd> <dt>

*plMax* \[ à\]
</dt> <dd>

Valeur maximale valide pour la propriété d’entrée.

</dd> <dt>

*plSteppingDelta* \[ à\]
</dt> <dd>

Incrément par lequel la valeur de la propriété peut être augmentée ou diminuée.

</dd> <dt>

*plDefault* \[ à\]
</dt> <dd>

Valeur par défaut du paramètre de *propriété* .

</dd> <dt>

*plFlags* \[ à\]
</dt> <dd>

Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




