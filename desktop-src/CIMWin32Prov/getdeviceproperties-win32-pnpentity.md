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
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033649"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_PnPEntity Win32**](win32-pnpentity.md)
</dt> </dl>

 

 




