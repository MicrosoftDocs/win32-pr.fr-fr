---
description: La méthode GetCount récupère le nombre de clés de cette collection.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'IPortableDeviceKeyCollection :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404183"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a>IPortableDeviceKeyCollection :: GetCount, méthode

La méthode **GetCount** récupère le nombre de clés de cette collection.

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

Pointeur vers une **valeur DWORD** qui contient le nombre de clés dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>                     |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Un argument de pointeur obligatoire était **null**.<br/> |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Récupération des événements de service pris en charge](retrieving-supported-events.md)
</dt> <dt>

[Récupération des méthodes de service prises en charge](retrieving-supported-methods.md)
</dt> </dl>

 

 




