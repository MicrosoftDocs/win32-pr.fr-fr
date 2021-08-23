---
description: La méthode Set définit la valeur d’une propriété de contrôle de qualité d’appel donnée.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'ITCallQualityControl :: Set, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5506e4c318440c2b611a2404590bdf638d34a7da2353a5598d09aecf2990668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003387"
---
# <a name="itcallqualitycontrolset-method"></a>ITCallQualityControl :: Set, méthode

\[cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **Set** définit la valeur d’une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Propriété* \[ dans\]
</dt> <dd>

Membre de l’énumération [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*lValue* \[ dans\]
</dt> <dd>

Valeur souhaitée pour la propriété.

</dd> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* doit être contrôlée.

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

 

 




