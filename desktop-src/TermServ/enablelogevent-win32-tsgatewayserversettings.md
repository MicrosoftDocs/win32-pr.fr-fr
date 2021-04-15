---
title: Méthode EnableLogEvent de la classe Win32_TSGatewayServerSettings
description: Active ou désactive la journalisation du type d’événement spécifié.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableLogEvent
- Services Bureau à distance de la méthode EnableLogEvent, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableLogEvent
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467042"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode EnableLogEvent de la \_ classe Win32 TSGatewayServerSettings

Active ou désactive la journalisation du type d’événement spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EventName* \[ dans\]
</dt> <dd>

Nom de l’événement. Cette valeur doit être récupérée à l’aide de la méthode [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .

<dt>

LogChannelDisconnect
</dt> <dd>

L’utilisateur a réussi à se déconnecter de la ressource.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

L’utilisateur n’a pas pu se connecter à la ressource.

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

L’utilisateur n’a pas d’autorisation de connexion.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

L’utilisateur n’a pas d’autorisation de ressource.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

L’utilisateur a réussi à se connecter à la ressource.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

L’utilisateur a réussi à réussir l’autorisation de connexion.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

L’utilisateur a réussi à réussir l’autorisation des ressources.

</dd> </dl> </dd> <dt>

*Activé* \[ dans\]
</dt> <dd>

Spécifie si l’événement doit être activé ou désactivé.

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

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

