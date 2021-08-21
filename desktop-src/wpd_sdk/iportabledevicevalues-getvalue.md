---
description: La méthode GetValue récupère une valeur PROPVARIANT spécifiée par une clé.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'IPortableDeviceValues :: GetValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cce387bfc08c48547603d8b30a3952952f1e2decf70e06986ea4fb477fe4fdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843031"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>IPortableDeviceValues :: GetValue, méthode

La méthode **GetValue** récupère une valeur **PROPVARIANT** spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.

</dd> <dt>

*pValue* \[ à\]
</dt> <dd>

Pointeur vers la valeur **PROPVARIANT** récupérée. L’appelant doit libérer la mémoire en appelant **PropVariantClear** lorsqu’il est terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                     |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/> |



 

## <a name="remarks"></a>Remarques

Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la récupération d'  une mémoire tampon de taille nulle ou nulle n’est pas prise en charge. Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.

Cette méthode peut être utilisée pour récupérer une valeur de n’importe quel type de la collection. Toutefois, si vous connaissez le type de valeur à l’avance, utilisez l’une des méthodes de récupération spécialisées de cette interface pour éviter la surcharge de travail avec les valeurs PROPVARIANT directement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues :: SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




