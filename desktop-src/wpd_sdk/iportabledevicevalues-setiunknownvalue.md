---
description: La méthode SetIUnknownValue ajoute une nouvelle valeur IUnknown (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'IPortableDeviceValues :: SetIUnknownValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c4a7c8a77cfef505b2a507b6281b931eea7f09c4ea1fbc79e651e7f517593799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697050"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a>IPortableDeviceValues :: SetIUnknownValue, méthode

La méthode **SetIUnknownValue** ajoute une nouvelle valeur **IUnknown** (type VT \_ inconnu) ou remplace celle qui existe déjà.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
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

Pointeur vers une interface **IUnknown** qui spécifie la nouvelle valeur. Le kit de développement logiciel (SDK) copie une référence à l’interface envoyée et appelle **AddRef** dessus.

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

[**IPortableDeviceValues::GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




