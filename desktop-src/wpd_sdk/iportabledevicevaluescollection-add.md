---
description: 'IPortableDeviceValuesCollection :: Add, méthode-la méthode Add ajoute un élément à la collection.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'IPortableDeviceValuesCollection :: Add, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9cc105ae553d78dd6c8a12219be8e2c42cba1e236c25a0392457b36553bd4e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839319"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>IPortableDeviceValuesCollection :: Add, méthode

La méthode **Add** ajoute un élément à la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pValues* \[ dans\]
</dt> <dd>

Pointeur vers une interface **IPortableDeviceValues** à ajouter à la collection. L’interface n’est pas réellement copiée, mais **AddRef** est appelé dessus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                   | Description                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | S_OK<br/>                                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour ajouter la valeur à la collection.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




