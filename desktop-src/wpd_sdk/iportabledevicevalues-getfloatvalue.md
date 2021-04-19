---
description: La méthode GetFloatValue récupère une valeur FLOTTante (type VT \_ R4) spécifiée par une clé.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'IPortableDeviceValues :: GetFloatValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520909"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>IPortableDeviceValues :: GetFloatValue, méthode

La méthode **getFloatValue** récupère une valeur **flottante** (type VT \_ R4) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
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

Pointeur vers la valeur **float** récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                             | Description                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | S_OK<br/>                                     |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>    | La propriété spécifiée par la *clé* n’est pas un type **float** .<br/>  |
| <dl> <dt>**\_ID prop \_ \_ non pris en charge**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetFloatValue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




