---
title: Classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Décrit une stratégie d’autorisation des connexions Bureau à distance (RD \ 160 ; CAP). RD \ 160 ; Les limites sont utilisées pour déterminer si un utilisateur est autorisé à se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfaefb0a3062db27622afe90023928507c6d127c64edb60041347f73c1b261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349244"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>\_Classe TSGatewayConnectionAuthorizationPolicy Win32

Décrit une stratégie d’autorisation de connexion Bureau à distance. Les limitations des services Bureau à distance sont utilisées pour déterminer si un utilisateur est autorisé à se connecter au serveur de passerelle Bureau à distance (passerelle Bureau à distance).

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** possède ces méthodes.



| Méthode                                                                                                                | Description                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Ajoute les noms de groupes d’ordinateurs spécifiés à la propriété **ComputerGroupNames** .<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Ajoute les noms de groupes d’utilisateurs spécifiés à la propriété **UserGroupNames** .<br/>                                                                                              |
| [**Créer**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Crée une stratégie d’autorisation des connexions aux services Bureau à distance<br/>                                                                                                                                                   |
| [**Supprimer**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Supprime la stratégie d’autorisation des connexions aux services Bureau à distance actuelle.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Définit la propriété **ClipboardDisabled** .<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Définit la propriété **DiskDrivesDisabled** .<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Définit la propriété **PlugAndPlayDevicesDisabled** .<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Définit la propriété **PrintersDisabled** .<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Définit la propriété **SerialPortsDisabled** .<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Utilisé pour basculer la propriété **AllowOnlySDRServers**<br/> **Windows Server 2008 :** cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                  |
| [**Descendre**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Déplace la position de la stratégie d’autorisation des connexions aux services Bureau à distance active vers le début dans la liste.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Déplace la position de la stratégie d’autorisation des connexions aux services Bureau à distance actuelle vers le haut dans la liste.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Supprime les noms de groupes d’ordinateurs spécifiés de la propriété **ComputerGroupNames** .<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Supprime les noms de groupes d’utilisateurs spécifiés de la propriété **UserGroupNames** .<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Définit la propriété **ComputerGroupNames** .<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Définit la propriété **CookieAuthenticationAllowed** .<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Définit la propriété **DeviceRedirectionType** .<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Active ou désactive la stratégie d’autorisation des connexions aux services Bureau à distance actuelle.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Définit la propriété **IdleTimeout** .<br/> **Windows Server 2008 :** cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Définit un nouveau nom pour cette stratégie d’autorisation des connexions aux services Bureau à distance. Cette méthode garantit que les noms seront uniques.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Définit la propriété **PasswordAllowed** .<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Définit la propriété **SecureIdAllowed** .<br/> **Windows Server 2008 :** Cette méthode est réservée à une utilisation ultérieure.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Définit les propriétés **SessionTimeout** et **SessionTimeoutAction** .<br/> **Windows Server 2008 :** cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Définit la propriété **SmartcardAllowed** .<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Définit la propriété **UserGroupNames** .<br/>                                                                                                                                |
| [**Update**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Met à jour la stratégie d’autorisation des connexions aux services Bureau à distance actuelle.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** a ces propriétés.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les connexions sont autorisées uniquement pour sécuriser les serveurs RDS de redirection des appareils (SDR). Cette propriété peut être définie à l’aide de la méthode [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .

**Windows Server 2008 :** cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la redirection du presse-papiers est désactivée. Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des noms de groupes d’ordinateurs séparés par des points-virgules. Cette valeur peut être vide. Les noms sont au format *domaine \\ ComputerGroupName*. Si une valeur est spécifiée, l’ordinateur client doit appartenir à l’un de ces groupes d’ordinateurs pour que l’utilisateur accède au serveur de passerelle Bureau à distance.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’authentification par cookie peut être utilisée pour se connecter au serveur de passerelle Bureau à distance. Cette propriété peut être définie à l’aide de la méthode [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les appareils qui seront redirigés.

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

Les appareils spécifiés ne seront pas redirigés. Les propriétés **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** et **PlugAndPlayDevicesDisabled** contrôlent les appareils qui ne seront pas redirigés.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la redirection de lecteur de disque est désactivée. Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».

</dd> <dt>

**Activé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si cette limite d’accès aux services Bureau à distance sera utilisée pour évaluer l’autorisation d’un utilisateur.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les connexions aux services Bureau à distance utilisent des attributs de protection d’accès réseau (NAP).

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur du délai d’inactivité en minutes. La valeur 0 signifie qu’il n’y a aucun délai d’attente. Cette propriété peut être définie à l’aide de la méthode [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom de la stratégie d’autorisation des connexions aux services Bureau à distance.

</dd> <dt>

**Commande**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Ordre d’évaluation de la stratégie d’autorisation des connexions aux services Bureau à distance. La première valeur d’évaluation des connexions aux services Bureau à distance a la valeur « 1 ». La propriété **Order** peut être modifiée lors de l’appel des méthodes [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)ou [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si un mot de passe peut être utilisé pour se connecter au serveur de passerelle Bureau à distance. Cette propriété peut être modifiée à l’aide de la méthode [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la redirection des appareils Plug-and-Plays est désactivée. Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».

</dd> <dt>

**PrintersDisabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la redirection d’imprimante est désactivée. Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si un identificateur sécurisé peut être utilisé pour se connecter au serveur de passerelle Bureau à distance.

**Windows Server 2008 :** Cette propriété n’est pas utilisée.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la redirection de port série est désactivée. Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

La valeur du délai d’expiration de session, en minutes. La valeur 0 signifie qu’il n’y a aucun délai d’attente. Cette propriété peut être définie à l’aide de la méthode [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’action à entreprendre dans le cas d’un délai d’expiration de session. Cette propriété peut être définie à l’aide de la méthode [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

Il peut s’agir de l’une des valeurs suivantes.

**Windows Server 2008 :** Cette propriété n’est pas disponible.

<dt>

0
</dt> <dd>

Déconnectez la session.

</dd> <dt>

1
</dt> <dd>

Essayez de réautoriser la session.

</dd> </dl>

</dd> <dt>

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si une carte à puce peut être utilisée pour se connecter au serveur de passerelle Bureau à distance. Cette propriété peut être modifiée à l’aide de la méthode [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des noms de groupes d’utilisateurs séparés par des points-virgules. Les noms sont au format *domaine \\ UserGroupName*. Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’utilisateur est autorisé à accéder au serveur de passerelle Bureau à distance.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour utiliser cette classe, vous devez être membre du groupe administrateurs.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

