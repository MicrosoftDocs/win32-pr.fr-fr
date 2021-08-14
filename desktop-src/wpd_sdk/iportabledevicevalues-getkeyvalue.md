---
description: La méthode GetKeyValue récupère une valeur PROPERTYKEY spécifiée par une clé.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'IPortableDeviceValues :: GetKeyValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fb22fa8f93365cb7b0bc1f29b479683728b508a973a8702f5b86cc2605d0445d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194019"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a>IPortableDeviceValues :: GetKeyValue, méthode

La méthode **GetKeyValue** récupère une valeur **PROPERTYKEY** spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.

</dd> <dt>

*pValue* \[ à\]
</dt> <dd>

Pointeur vers la valeur **PROPERTYKEY** récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                          |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par *Key* n’est pas un type **PROPERTYKEY** .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/>      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetKeyValue**](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




