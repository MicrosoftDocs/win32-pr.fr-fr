---
description: La méthode GetBoolValue récupère une valeur booléenne (type VT \_ bool) spécifiée par une clé.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'IPortableDeviceValues :: GetBoolValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528703"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a>IPortableDeviceValues :: GetBoolValue, méthode

La méthode **GetBoolValue** récupère une valeur **BOOLÉENNE** (type VT \_ bool) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
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

Pointeur vers la valeur **booléenne** récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                     |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par la *clé* n’est pas un type **bool** .<br/>   |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/> |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [définition des propriétés d’un objet unique](setting-properties-for-a-single-object.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues :: SetBoolValue,**](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[Récupération des événements de service pris en charge](retrieving-supported-events.md)
</dt> <dt>

[Définition des propriétés d’un objet unique](setting-properties-for-a-single-object.md)
</dt> <dt>

[Écriture de propriétés Content-Object](writing-content-object-properties.md)
</dt> </dl>

 

 




