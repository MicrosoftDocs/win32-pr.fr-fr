---
description: La méthode GetType récupère le type de données des éléments de la collection.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'IPortableDevicePropVariantCollection :: GetType, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541321"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>IPortableDevicePropVariantCollection :: GetType, méthode

La méthode **GetType** récupère le type de données des éléments de la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Pvt* \[ à\]
</dt> <dd>

Valeur d’énumération **VarType** du kit de développement Platform SDK qui indique le type de données de tous les éléments de la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>                     |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Un argument de pointeur obligatoire était **null**.<br/> |



 

## <a name="remarks"></a>Notes

Tous les éléments stockés dans un **IPortableDevicePropVariantCollection** sont du même type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




