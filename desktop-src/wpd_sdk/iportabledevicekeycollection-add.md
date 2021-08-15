---
description: La méthode Add ajoute une clé de propriété à la collection.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'IPortableDeviceKeyCollection :: Add, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6aa28a7a8a6439f27a095033d35e8b066c1488af13d1ade921f16c4143843adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194719"
---
# <a name="iportabledevicekeycollectionadd-method"></a>IPortableDeviceKeyCollection :: Add, méthode

La méthode **Add** ajoute une clé de propriété à la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** à ajouter à la collection. Cette méthode copie la clé dans la collection, ce qui vous permet de libérer la variable locale après avoir appelé cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                   | Description                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | S_OK<br/>                                                  |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour ajouter la clé à la collection.<br/> |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des propriétés pour un seul objet](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Récupération des propriétés Content-Object](retrieving-content-object-properties.md)
</dt> <dt>

[Récupération des propriétés d’un objet unique](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




