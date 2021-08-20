---
description: Obtient les propriétés spécifiées de cette Plug-and-Play appareil.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Méthode GetDeviceProperties de la classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 855c3c0644d8c7b5c5300c8d12d5a6f98073a4511f8d0d65f4058da7fb9d0f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077509"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Méthode GetDeviceProperties de la \_ classe Win32 PnPEntity

Obtient les propriétés spécifiées de cette Plug-and-Play appareil.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*devicePropertyKeys* \[ dans, facultatif\]
</dt> <dd>

Propriétés à retourner.

</dd> <dt>

*deviceProperties* \[ à\]
</dt> <dd>

Propriétés demandées dans les sous-types appropriés de la classe abstraite [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_PnPEntity Win32**](win32-pnpentity.md)
</dt> </dl>

 

 




