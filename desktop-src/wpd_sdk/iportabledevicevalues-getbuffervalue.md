---
description: La méthode GetBufferValue récupère une valeur de tableau d’octets (type \_ VT \| VT \_ UI1) spécifiée par une clé.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'IPortableDeviceValues :: GetBufferValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c5d209d7ee13f55ab2236166851e2e24143b9cdeb01e947f0463491eb7446eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963698"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>IPortableDeviceValues :: GetBufferValue, méthode

La méthode **GetBufferValue** récupère une valeur de **tableau d’octets** (type VT \_ \| VT \_ UI1) spécifiée par une clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.

</dd> <dt>

*ppValue* \[ à\]
</dt> <dd>

Pointeur vers la **valeur d’octet \* *_ récupérée. L’appelant est chargé de libérer la mémoire en appelant _* CoTaskMemFree**.

</dd> <dt>

*pcbValue* \[ à\]
</dt> <dd>

Pointeur vers la taille de *ppValue*, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | S_OK<br/>                                     |
| <dl> <dt>**\_TYPEMISMATCH DISP \_**</dt> </dl>                   | La propriété spécifiée par la *clé* n’est pas un type **Byte** \* .<br/> |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt> </dl> | La propriété spécifiée par la *clé* ne figure pas dans la collection.<br/> |



 

## <a name="remarks"></a>Remarques

La récupération d’une mémoire tampon **null** ou d’une mémoire tampon de taille zéro n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBufferValue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




