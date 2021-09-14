---
description: La méthode GetIPortableDeviceValuesCollectionValue récupère une valeur IPortableDeviceValuesCollection (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'IPortableDeviceValues :: GetIPortableDeviceValuesCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293103"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>IPortableDeviceValues :: GetIPortableDeviceValuesCollectionValue, méthode

La méthode **GetIPortableDeviceValuesCollectionValue** récupère une valeur **IPORTABLEDEVICEVALUESCOLLECTION** (type VT \_ inconnu) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
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

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) récupérée. L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                                                    |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par *Key* n’est pas une interface **IPortableDeviceValuesCollection** .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/>                                |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[Récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




