---
description: La méthode GetUnsignedIntegerValue récupère une valeur ULONG (type VT \_ UI4) spécifiée par une clé.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'IPortableDeviceValues :: GetUnsignedIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: eeb418d3d0aa42675f3d5766f2a8d08e1ad2377bbaa4a2a07f4ba96524d3dec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026837"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a>IPortableDeviceValues :: GetUnsignedIntegerValue, méthode

La méthode **GetUnsignedIntegerValue** récupère une valeur **ULong** (type VT \_ UI4) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
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

Pointeur vers la valeur **ULong** récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                     |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par la *clé* n’est pas un type **ULong** .<br/>  |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/> |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[Récupération des événements de service pris en charge](retrieving-supported-events.md)
</dt> <dt>

[Récupération des méthodes de service prises en charge](retrieving-supported-methods.md)
</dt> <dt>

[Récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




