---
description: La méthode RemoveAt supprime l’élément stocké à l’emplacement spécifié par l’index donné.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'IPortableDevicePropVariantCollection :: RemoveAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520839"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>IPortableDevicePropVariantCollection :: RemoveAt, méthode

La méthode **RemoveAt** supprime l’élément stocké à l’emplacement spécifié par l’index donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Spécifie l’index de l’élément à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’index spécifié était hors limites.<br/> |



 

## <a name="remarks"></a>Notes

Vous devez spécifier un index de base zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




