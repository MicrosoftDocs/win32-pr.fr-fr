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
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520984"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                             |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par la *clé* n’est pas une interface **IUnknown** .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/>         |



 

## <a name="requirements"></a>Spécifications



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

 

 




