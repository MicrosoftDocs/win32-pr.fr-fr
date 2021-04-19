---
description: La méthode GetIPortableDeviceKeyCollectionValue récupère une valeur IPortableDeviceKeyCollection (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535990"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue, méthode

La méthode **GetIPortableDeviceKeyCollectionValue** récupère une valeur **IPORTABLEDEVICEKEYCOLLECTION** (type VT \_ inconnu) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.

</dd> <dt>

*ppValue* \[ à\]
</dt> <dd>

Pointeur vers le pointeur d’interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) récupéré. L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                                                 |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par *Key* n’est pas une interface **IPortableDeviceKeyCollection** .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/>                             |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Récupération des événements de service pris en charge](retrieving-supported-events.md)
</dt> <dt>

[Récupération des méthodes de service prises en charge](retrieving-supported-methods.md)
</dt> </dl>

 

 




