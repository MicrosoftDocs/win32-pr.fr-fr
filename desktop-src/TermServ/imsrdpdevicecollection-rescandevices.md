---
title: Méthode IMsRdpDeviceCollection RescanDevices
description: Actualise la liste des objets dans la collection. | Méthode IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RescanDevices
- Méthode RescanDevices Services Bureau à distance, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, méthode RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959239"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>IMsRdpDeviceCollection :: RescanDevices, méthode

Actualise la liste des objets dans la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vboolDynRedir* \[ dans\]
</dt> <dd>

État de redirection par défaut qui sera appliqué aux périphériques ou lecteurs récemment découverts.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





