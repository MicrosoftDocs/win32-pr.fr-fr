---
description: La méthode GetAt récupère une valeur de la collection à l’aide de l’index de base zéro fourni.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'IPortableDeviceValues :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843022"
---
# <a name="iportabledevicevaluesgetat-method"></a>IPortableDeviceValues :: GetAt, méthode

La méthode **GetAt** récupère une valeur de la collection à l’aide de l’index de base zéro fourni.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Valeur DWORD** qui spécifie un index de base zéro dans la collection.

</dd> <dt>

A-la  \[ in, out\]
</dt> <dd>

Pointeur **PROPERTYKEY** facultatif qui récupère la clé de l’élément spécifié.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

**PROPVARIANT** facultatif qui récupère la valeur de l’élément spécifié. L’appelant doit libérer la mémoire en appelant **PropVariantClear** lorsqu’il est terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un numéro d’index non valide a été spécifié.<br/> |



 

## <a name="remarks"></a>Remarques

si une propriété indique une valeur de type VT \_ inconnu, la propriété sera l’un des Windows appareils mobiles ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) ou [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). aucune autre interface ne peut être retournée par Windows appareils mobiles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




