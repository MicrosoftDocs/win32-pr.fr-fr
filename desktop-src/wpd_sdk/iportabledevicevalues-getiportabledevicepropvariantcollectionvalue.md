---
description: La méthode GetIPortableDevicePropVariantCollectionValue récupère une valeur IPortableDevicePropVariantCollection (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'IPortableDeviceValues :: GetIPortableDevicePropVariantCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294395"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a>IPortableDeviceValues :: GetIPortableDevicePropVariantCollectionValue, méthode

La méthode **GetIPortableDevicePropVariantCollectionValue** récupère une valeur **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (type VT \_ inconnu) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
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

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) récupérée. L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                                                         |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par *Key* n’est pas une interface **IPortableDevicePropVariantCollection** .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/>                                     |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




