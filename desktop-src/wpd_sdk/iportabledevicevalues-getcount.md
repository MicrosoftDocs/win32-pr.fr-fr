---
description: 'IPortableDeviceValues :: GetCount, méthode-la méthode GetCount récupère le nombre d’éléments de la collection.'
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'IPortableDeviceValues :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086237"
---
# <a name="iportabledevicevaluesgetcount-method"></a>IPortableDeviceValues :: GetCount, méthode

La méthode **GetCount** récupère le nombre d’éléments dans la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcelt* \[ dans\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui contient le nombre d’éléments dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> </dl>

 

 




