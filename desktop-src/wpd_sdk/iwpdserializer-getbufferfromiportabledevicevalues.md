---
description: La méthode GetBufferFromIPortableDeviceValues sérialise une interface IPortableDeviceValues soumise à un tableau d’octets alloué. Le tableau d’octets retourné est alloué pour l’appelant et doit être libéré par l’appelant à l’aide de CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'IWpdSerializer :: GetBufferFromIPortableDeviceValues, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525140"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>IWpdSerializer :: GetBufferFromIPortableDeviceValues, méthode

La méthode **GetBufferFromIPortableDeviceValues** sérialise une interface **IPortableDeviceValues** soumise à un tableau d’octets alloué. Le tableau d’octets retourné est alloué pour l’appelant et doit être libéré par l’appelant à l’aide de **CoTaskMemFree**.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSource* \[ dans\]
</dt> <dd>

Pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) à sérialiser.

</dd> <dt>

*ppBuffer* \[ à\]
</dt> <dd>

Pointeur vers un **octet \* *_ qui contient les données sérialisées. Windows Les périphériques portables allouent cette mémoire ; l’appelant doit le libérer en appelant _* CoTaskMemFree**.

</dd> <dt>

*pdwBufferSize* \[ à\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui spécifie la taille de la mémoire tampon allouée, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                   | Description                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | S_OK<br/>                                       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un argument de pointeur obligatoire était **null**.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire disponible insuffisante pour créer la mémoire tampon.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




