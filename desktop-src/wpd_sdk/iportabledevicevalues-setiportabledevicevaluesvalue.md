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
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539621"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

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

 

 




