---
description: La méthode WriteIPortableDeviceValuesToBuffer sérialise une interface IPortableDeviceValues dans un tableau d’octets alloué par l’appelant.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'IWpdSerializer :: WriteIPortableDeviceValuesToBuffer, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: db86953e2e08c0a66f6e497c1fcd2350cc726be8852803cf8f4d64bfff523500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657739"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>IWpdSerializer :: WriteIPortableDeviceValuesToBuffer, méthode

La méthode **WriteIPortableDeviceValuesToBuffer** sérialise une interface **IPortableDeviceValues** dans un tableau d’octets alloué par l’appelant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwOutputBufferLength* \[ dans\]
</dt> <dd>

**Valeur DWORD** qui spécifie la taille de *pbuffer*, en octets.

</dd> <dt>

*pResults* \[ dans\]
</dt> <dd>

Pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) à sérialiser.

</dd> <dt>

*pbuffer* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant. Pour connaître la taille de la mémoire tampon requise, appelez **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ à\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui indique le nombre d’octets réellement écrits dans la mémoire tampon allouée par l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                   | Description                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | S_OK<br/>                          |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un argument de pointeur obligatoire était **null**.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire tampon fournie par l’appelant n’est pas assez grande.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode copie une interface **IPortableDeviceValues** dans une mémoire tampon existante. Si vous souhaitez allouer une nouvelle mémoire tampon, utilisez [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




