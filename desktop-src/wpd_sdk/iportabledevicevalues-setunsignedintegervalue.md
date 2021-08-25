---
description: La méthode SetUnsignedIntegerValue ajoute une nouvelle valeur ULONG (type VT \_ UI4) ou remplace celle qui existe déjà.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'IPortableDeviceValues :: SetUnsignedIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9c58569554cf9170788524bdcb233bf42b3318f1e954050bb713711c93337543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928459"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a>IPortableDeviceValues :: SetUnsignedIntegerValue, méthode

La méthode **SetUnsignedIntegerValue** ajoute une nouvelle valeur **ULong** (type VT \_ UI4) ou remplace celle qui existe déjà.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

**ULong** qui spécifie la nouvelle valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [**spécification des informations sur le client**](specifying-client-information.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[**Spécification des informations sur le client**](specifying-client-information.md)
</dt> </dl>

 

 




