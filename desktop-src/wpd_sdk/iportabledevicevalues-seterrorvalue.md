---
description: La méthode SetErrorValue ajoute une nouvelle valeur HRESULT (type VT \_ Error) ou remplace une valeur existante.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'IPortableDeviceValues :: SetErrorValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 41bb9a6d8f2878b9bcfac6584c39fd55153ecae8a539c7f8886a5d0eb90d1bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026787"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a>IPortableDeviceValues :: SetErrorValue, méthode

La méthode **SetErrorValue** ajoute une nouvelle valeur **HRESULT** (type VT \_ Error) ou remplace une valeur existante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
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

**HRESULT** qui contient la nouvelle valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetErrorValue**](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




