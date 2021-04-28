---
description: 'IPortableDevicePropVariantCollection :: Add, méthode-la méthode Add ajoute un élément à la collection.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'IPortableDevicePropVariantCollection :: Add, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112457"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>IPortableDevicePropVariantCollection :: Add, méthode

La méthode **Add** ajoute un élément à la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pValue* \[ dans\]
</dt> <dd>

Pointeur vers un nouvel objet **PROPVARIANT** à ajouter à la collection. Cette méthode copie le **PROPVARIANT** dans la collection. vous devez donc libérer votre copie locale de la variable en appelant **PropVariantClear** après avoir appelé cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes 

Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la définition et la récupération  d’une mémoire tampon de taille zéro ou nulle ne sont pas prises en charge. Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.

Si un appelant tente d’ajouter un élément d’un autre VARTYPE contenu dans la collection et que la valeur PROPVARIANT ne peut pas être modifiée automatiquement par cette interface, cette méthode échoue. Pour modifier manuellement le type de collection, appelez [**IPortableDevicePropVariantCollection :: ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération d’un identificateur d’objet à partir d’un identificateur unique persistant](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Déplacement du contenu sur l’appareil](moving-content-on-the-device.md)
</dt> <dt>

[Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




