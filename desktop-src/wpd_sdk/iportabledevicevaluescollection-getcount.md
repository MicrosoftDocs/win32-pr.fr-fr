---
description: La méthode GetCount récupère le nombre d’éléments dans la collection.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'IPortableDeviceValuesCollection :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525134"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>IPortableDeviceValuesCollection :: GetCount, méthode

La méthode **GetCount** récupère le nombre d’éléments dans la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcElems* \[ dans\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui contient le nombre d’interfaces **IPortableDeviceValues** dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>                     |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Un argument de pointeur obligatoire était **null**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




