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
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525133"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                   | Description                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | S_OK<br/>                          |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un argument de pointeur obligatoire était **null**.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire tampon fournie par l’appelant n’est pas assez grande.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode copie une interface **IPortableDeviceValues** dans une mémoire tampon existante. Si vous souhaitez allouer une nouvelle mémoire tampon, utilisez [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




