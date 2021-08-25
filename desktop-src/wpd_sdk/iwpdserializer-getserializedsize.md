---
description: La méthode GetSerializedSize calcule la taille de la mémoire tampon requise pour contenir une interface IPortableDeviceValues sérialisée.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'IWpdSerializer :: GetSerializedSize, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae6b8381928c64b7d16e9f5daa4dd9fd85acd9b61c13531365d871563ef6afe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704519"
---
# <a name="iwpdserializergetserializedsize-method"></a>IWpdSerializer :: GetSerializedSize, méthode

La méthode **GetSerializedSize** calcule la taille de la mémoire tampon requise pour contenir une interface [**IPortableDeviceValues**](iportabledevicevalues.md) sérialisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSource* \[ dans\]
</dt> <dd>

Pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) dont vous souhaitez demander la taille.

</dd> <dt>

*pdwSize* \[ à\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui indique la taille de la mémoire tampon requise pour sérialiser *pSource*, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                   | Description                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | S_OK<br/>                                       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un argument de pointeur obligatoire était **null**.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour créer la mémoire tampon.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




