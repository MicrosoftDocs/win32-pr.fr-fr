---
description: La méthode SetUnsignedLargeIntegerValue ajoute une nouvelle valeur ULONGLONG (type VT \_ UI8) ou remplace celle qui existe déjà.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'IPortableDeviceValues :: SetUnsignedLargeIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541071"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a>IPortableDeviceValues :: SetUnsignedLargeIntegerValue, méthode

La méthode **SetUnsignedLargeIntegerValue** ajoute une nouvelle valeur **ULONGLONG** (type VT \_ UI8) ou remplace celle qui existe déjà.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

**ULONGLONG** qui spécifie la nouvelle valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Ajout d’une ressource à un objet](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




