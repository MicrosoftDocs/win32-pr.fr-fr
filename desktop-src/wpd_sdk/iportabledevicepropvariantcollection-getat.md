---
description: 'IPortableDevicePropVariantCollection :: GetAt, méthode-la méthode GetAt récupère un élément de la collection à l’aide d’un index de base zéro.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'IPortableDevicePropVariantCollection :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 02fa273b3bedea78884e15d2dedb5b7d2f675c78330c735e3bfb1896bc9d5199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963728"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>IPortableDevicePropVariantCollection :: GetAt, méthode

La méthode **GetAt** récupère un élément de la collection à l’aide d’un index de base zéro.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

**Valeur DWORD** qui contient l’index de base zéro de l’élément à récupérer.

</dd> <dt>

*pValue* \[ à\]
</dt> <dd>

Pointeur vers une structure **PROPVARIANT** . L’appelant est chargé de libérer cette mémoire en appelant **PropVariantClear**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                          |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Un argument de pointeur obligatoire était **null**.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’index qui a été passé était hors limites.<br/> |



 

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

[Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Récupération des événements de service pris en charge](retrieving-supported-events.md)
</dt> <dt>

[Récupération des formats de service pris en charge](retrieving-supported-formats.md)
</dt> <dt>

[Récupération des méthodes de service prises en charge](retrieving-supported-methods.md)
</dt> <dt>

[Récupération des types de contenu pris en charge par un appareil](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Récupération des identificateurs d’objets fonctionnels pour un appareil](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Définition des propriétés de plusieurs objets](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




