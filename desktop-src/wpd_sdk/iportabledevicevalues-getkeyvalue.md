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
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540425"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



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

 

 




