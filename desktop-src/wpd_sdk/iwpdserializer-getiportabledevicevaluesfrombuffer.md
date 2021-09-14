---
description: La méthode GetIPortableDeviceValuesFromBuffer désérialise un tableau d’octets en une interface IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'IWpdSerializer :: GetIPortableDeviceValuesFromBuffer, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219377"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>IWpdSerializer :: GetIPortableDeviceValuesFromBuffer, méthode

La méthode **GetIPortableDeviceValuesFromBuffer** désérialise un tableau d’octets en une interface **IPortableDeviceValues** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbuffer* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon à désérialiser.

</dd> <dt>

*dwInputBufferLength* \[ dans\]
</dt> <dd>

**Valeur DWORD** qui spécifie la taille de la mémoire tampon, en octets.

</dd> <dt>

*ppParams* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) créée à partir de la mémoire tampon. L’application est chargée d’appeler la **version Release** sur l’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                     |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Un argument de pointeur obligatoire était **null**.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Une erreur de conversion non spécifiée s’est produite.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




