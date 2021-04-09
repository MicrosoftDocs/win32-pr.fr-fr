---
title: Méthode SetNetworkAdapterLanaID de la classe Win32_TSNetworkAdapterSetting
description: Spécifie le numéro de carte réseau local (LANA) de la carte réseau à définir.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetNetworkAdapterLanaID
- Services Bureau à distance de la méthode SetNetworkAdapterLanaID, classe Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, méthode SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743493"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Méthode SetNetworkAdapterLanaID de la \_ classe Win32 TSNetworkAdapterSetting

La méthode **SetNetworkAdapterLanaID** spécifie le numéro de carte réseau local (Lana) de la carte réseau à définir. Si l’ID de LANA spécifié n’est pas valide ou n’existe pas, une erreur est retournée. La liste disponible des ID de carte LANA est obtenue en énumérant la propriété **DeviceIDList** dans la classe [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NetworkAdapterLanaID* \[ dans\]
</dt> <dd>

Numéro LANA de la carte réseau à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

