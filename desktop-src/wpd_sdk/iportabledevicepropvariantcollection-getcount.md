---
description: La méthode GetCount récupère le nombre d’éléments de cette collection.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'IPortableDevicePropVariantCollection :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2b82ce3c916df3603478888ecdc388e80ee4b4d635a25b238f9ba6a03ef61901
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055199"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a>IPortableDevicePropVariantCollection :: GetCount, méthode

La méthode **GetCount** récupère le nombre d’éléments de cette collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcElems* \[ dans\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui contient le nombre d’éléments dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>                     |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Un argument de pointeur obligatoire était **null**.<br/> |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode [, consultez récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Récupération des événements de service pris en charge](retrieving-supported-events.md)
</dt> <dt>

[Récupération des formats de service pris en charge](retrieving-supported-formats.md)
</dt> <dt>

[Récupération des méthodes de service prises en charge](retrieving-supported-methods.md)
</dt> <dt>

[Récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Définition des propriétés de plusieurs objets](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




