---
title: Méthode EnumAuthorizationPlugins de la classe Win32_TSGatewayServerSettings
description: Énumère tous les plug-ins d’autorisation inscrits.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnumAuthorizationPlugins
- Services Bureau à distance de la méthode EnumAuthorizationPlugins, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnumAuthorizationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d955c08f5e4f91547751b0f177681ad2abd57c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844378"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode EnumAuthorizationPlugins de la \_ classe Win32 TSGatewayServerSettings

Énumère tous les plug-ins d’autorisation inscrits.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PluginNames* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de **chaînes** qui reçoit les noms des plug-ins d’autorisation inscrits.

</dd> <dt>

*CLSID* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de **chaînes** qui reçoit les CLSID des plug-ins d’autorisation inscrits.

</dd> <dt>

*Descriptions* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de **chaînes** qui reçoit les descriptions des plug-ins d’autorisation inscrits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                        |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

