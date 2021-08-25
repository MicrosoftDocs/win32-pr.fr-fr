---
description: La méthode ChangeType convertit tous les éléments de la collection au format VARTYPE spécifié.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'IPortableDevicePropVariantCollection :: ChangeType, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839329"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>IPortableDevicePropVariantCollection :: ChangeType, méthode

La méthode **ChangeType** convertit tous les éléments de la collection au format VarType spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VT* \[ dans\]
</dt> <dd>

Spécifie le **VarType** vers lequel vous souhaitez convertir tous les éléments de la collection. Les exemples de types incluent VT \_ UI4 et VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Si cette méthode échoue, la collection peut être laissée dans un état intermédiaire, avec certains membres convertis et certains non convertis.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




