---
title: Méthode DisableSerialPorts de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété SerialPortsDisabled.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisableSerialPorts
- Services Bureau à distance de la méthode DisableSerialPorts, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode DisableSerialPorts
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740413"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Méthode DisableSerialPorts de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy

Définit la propriété **SerialPortsDisabled** . Si la propriété **DeviceRedirectionType** a la valeur « 2 », la propriété **SerialPortsDisabled** contrôle la redirection des ports série pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Désactivé* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété **SerialPortsDisabled** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

