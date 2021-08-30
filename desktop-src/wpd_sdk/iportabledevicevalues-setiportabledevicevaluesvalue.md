---
description: La méthode SetIPortableDeviceValuesValue ajoute une nouvelle valeur IPortableDeviceValues (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'IPortableDeviceValues :: SetIPortableDeviceValuesValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44c5407deec49bb1b449ace87f3301912cd02b3e5d13a604f8725066e04c4ffb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930059"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a>IPortableDeviceValues :: SetIPortableDeviceValuesValue, méthode

La méthode **SetIPortableDeviceValuesValue** ajoute une nouvelle valeur **IPORTABLEDEVICEVALUES** (type VT \_ inconnu) ou remplace celle qui existe déjà.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.

</dd> <dt>

*pValue* \[ dans\]
</dt> <dd>

Pointeur vers une interface **IPortableDeviceValues** qui spécifie la nouvelle valeur. Le kit de développement logiciel (SDK) copie une référence à l’interface envoyée et appelle **AddRef** dessus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement. La mémoire clé existante est libérée de manière appropriée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




