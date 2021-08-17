---
description: La méthode GetIUnknownValue récupère une valeur d’interface IUnknown (type VT \_ Unknown) spécifiée par une clé.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'IPortableDeviceValues :: GetIUnknownValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: daf1164fefdc414a84508e4b295620af3cb671e9da624dd60cc08541c5c4fd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963648"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>IPortableDeviceValues :: GetIUnknownValue, méthode

La méthode **GetIUnknownValue** récupère une valeur d’interface **IUnknown** (type VT \_ Unknown) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
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

Adresse d’une variable qui reçoit un pointeur vers l’interface **IUnknown** récupérée. L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                             |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par la *clé* n’est pas une interface **IUnknown** .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/>         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




