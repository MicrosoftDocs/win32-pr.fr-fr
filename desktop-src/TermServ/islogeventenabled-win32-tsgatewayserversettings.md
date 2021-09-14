---
title: Méthode IsLogEventEnabled de la classe Win32_TSGatewayServerSettings
description: Indique si le type de journal des événements spécifié est activé.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLogEventEnabled
- Services Bureau à distance de la méthode IsLogEventEnabled, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193448"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode IsLogEventEnabled de la \_ classe Win32 TSGatewayServerSettings

Indique si le type de journal des événements spécifié est activé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EventName* \[ dans\]
</dt> <dd>

Nom du type de journal des événements. Cette valeur doit être récupérée à l’aide de la méthode [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .

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

*Activé* \[ à\]
</dt> <dd>

Indique si le type de journal des événements spécifié est activé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



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

 

