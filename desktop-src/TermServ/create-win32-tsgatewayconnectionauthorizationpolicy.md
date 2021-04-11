---
title: Créer une méthode de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Crée une stratégie d’autorisation de connexion Bureau à distance (RD \ 160 ; CAP) à l’aide des valeurs spécifiées. Le nouveau RD \ 160 ; Le capuchon est inséré en haut du Bureau à distance \ 160 ; Ordre d’évaluation CAP, avec la valeur de propriété Order \ 0034 ; 1 \ 0034 ;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_TSGatewayConnectionAuthorizationPolicy Class
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032525"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Créer une méthode de la \_ classe TSGatewayConnectionAuthorizationPolicy Win32

Crée une stratégie d’autorisation des connexions Bureau à distance (RD CAP) à l’aide des valeurs spécifiées. La nouvelle stratégie d’autorisation des connexions aux services Bureau à distance sera insérée en haut de l’ordre d’évaluation des connexions aux services Bureau à distance, avec une valeur de propriété de **commande** de « 1 ».

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nom de la stratégie d’autorisation des connexions aux services Bureau à distance. Le nom doit comporter 64 caractères ou moins, unique (la casse est ignorée) et ne peut pas contenir les caractères réservés suivants :

<>  :; " / \\ \| ? \*\[Onglet\]

</dd> <dt>

*UserGroupNames* \[ dans\]
</dt> <dd>

Liste des noms de groupes d’utilisateurs, séparés par des points-virgules, pour la nouvelle stratégie d’autorisation des connexions aux services Bureau à distance.

</dd> <dt>

*ComputerGroupNames* \[ dans\]
</dt> <dd>

Liste des noms de groupes d’ordinateurs, séparés par des points-virgules, pour la nouvelle stratégie d’autorisation des connexions aux services Bureau à distance.

</dd> <dt>

*Carte à puce* \[ dans\]
</dt> <dd>

Spécifie si les cartes à puce peuvent être utilisées pour l’authentification auprès du serveur de passerelle Bureau à distance.

</dd> <dt>

*Mot de passe* \[ dans\]
</dt> <dd>

Spécifie si les mots de passe peuvent être utilisés pour l’authentification auprès du serveur de passerelle Bureau à distance.

</dd> <dt>

*SecureId* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> <dt>

*Activé* \[ dans\]
</dt> <dd>

Spécifie si cette stratégie d’autorisation des connexions aux services Bureau à distance est activée.

</dd> <dt>

*DeviceRedirectionType* \[ dans\]
</dt> <dd>

Spécifie les types d’appareils qui seront redirigés.

<dt>

0
</dt> <dd>

Tous les appareils seront redirigés.

</dd> <dt>

1
</dt> <dd>

Aucun appareil n’est redirigé.

</dd> <dt>

2
</dt> <dd>

Les appareils spécifiés ne seront pas redirigés. Les paramètres *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* et *PlugAndPlayDevicesDisabled* contrôlent les appareils qui ne seront pas redirigés.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ dans\]
</dt> <dd>

Spécifie s’il faut désactiver la redirection de lecteur de disque si le paramètre *DeviceRedirectionType* est « 2 ».

</dd> <dt>

*PrintersDisabled* \[ dans\]
</dt> <dd>

Spécifie s’il faut désactiver la redirection de l’imprimante si le paramètre *DeviceRedirectionType* est « 2 ».

</dd> <dt>

*SerialPortsDisabled* \[ dans\]
</dt> <dd>

Spécifie s’il faut désactiver la redirection de port série si le paramètre *DeviceRedirectionType* est « 2 ».

</dd> <dt>

*ClipboardDisabled* \[ dans\]
</dt> <dd>

Spécifie s’il faut désactiver la redirection du presse-papiers si le paramètre *DeviceRedirectionType* est « 2 ».

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ dans\]
</dt> <dd>

Spécifie s’il faut désactiver la redirection des appareils Plug-and-Play si le paramètre *DeviceRedirectionType* est « 2 ».

</dd> <dt>

*IdleTimeout* \[ dans\]
</dt> <dd>

Valeur du délai d’inactivité en minutes

</dd> <dt>

*SessionTimeout* \[ dans\]
</dt> <dd>

Valeur du délai d’expiration de la session en minutes

</dd> <dt>

*SessionTimeoutAction* \[ dans\]
</dt> <dd>

Action du délai d’expiration de session en minutes

</dd> <dt>

*AllowOnlySDRServers* \[ dans\]
</dt> <dd>

Indique si les connexions sont autorisées uniquement pour les serveurs TS SDR

</dd> <dt>

*CookieAuthentication* \[ dans\]
</dt> <dd>

Indique si l’authentification par cookie peut être utilisée pour se connecter au serveur de passerelle TS

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

 

