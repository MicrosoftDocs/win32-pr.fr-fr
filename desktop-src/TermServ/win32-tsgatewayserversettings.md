---
title: Classe Win32_TSGatewayServerSettings
description: Fournit des méthodes et des propriétés permettant d’afficher et de configurer les paramètres du serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466706"
---
# <a name="win32_tsgatewayserversettings-class"></a>\_Classe TSGatewayServerSettings Win32

Fournit des méthodes et des propriétés permettant d’afficher et de configurer les paramètres du serveur de passerelle Bureau à distance (passerelle Bureau à distance). Un administrateur peut utiliser cette classe pour configurer un ensemble de protocoles, l’ensemble des événements qui seront écrits dans le journal des événements et le nombre maximal de connexions via la passerelle des services Bureau à distance.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayServerSettings** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayServerSettings** possède ces méthodes.



| Méthode                                                                                                                                             | Description                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurer**](configure-win32-tsgatewayserversettings.md)                                                                                       | Configure les paramètres IIS et RPC requis par le service de passerelle des services Bureau à distance.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Active ou désactive la propriété **CentralCAPEnabled** , qui détermine si des serveurs de stratégie d’autorisation de connexion centralisée Bureau à distance sont utilisés pour contrôler les stratégies d’autorisation de connexion pour ce serveur.<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Active ou désactive la journalisation du type d’événement spécifié.<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Définit la propriété **OnlyConsentCapableClients** .<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                                      |
| [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Cette méthode n’est pas prise en charge à partir de Windows Server 2016.<br/> **Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 et Windows server 2008 :** Active ou désactive les demandes pour une déclaration d’intégrité (SoH).<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Active ou désactive le transport spécifié.<br/> **Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Énumère tous les plug-ins d’authentification inscrits.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible.<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Énumère tous les plug-ins d’autorisation inscrits.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Obtient l’adresse IP d’écoute et le numéro de port pour le transport spécifié.<br/> **Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Retourne le nom d’événement du journal pour l’index d’événements de journal spécifié.<br/>                                                                                                                                                                                         |
| [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Retourne le nom de protocole pour l’index de protocole spécifié.<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Indique si le type de journal des événements spécifié est activé.<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Détermine si le transport spécifié est activé.<br/> **Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.<br/>                                                                        |
| [**QueryCertContext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Indique si le certificat spécifié est installé.<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Recycle les pools d’applications RPC dans IIS.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                                            |
| [**RefreshCertContext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Actualise le certificat utilisé par le serveur de passerelle Bureau à distance.<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance et recycle les pools d’applications RPC dans IIS.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Définit le plug-in d’autorisation actuel pour le serveur de passerelle Bureau à distance.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Définit le hachage de certificat pour la liaison HTTPs sur le port 443 dans IIS.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Définit les listes de contrôle d’accès (ACL) du certificat pour ce serveur.<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Définit les plug-ins d’authentification et d’autorisation actuels pour le serveur de passerelle Bureau à distance et recycle les pools d’applications RPC dans IIS.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Définit la propriété **EnforceChannelBinding** .<br/> **Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Définit l’adresse IP d’écoute et le numéro de port pour le transport spécifié.<br/> **Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Définit le nombre maximal de connexions autorisées via la passerelle des services Bureau à distance. Cette méthode modifie les propriétés **MaxConnections** et **UnlimitedConnections** .<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Définit le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Supprime le message d’administration pour le serveur de passerelle.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Supprime le message d’administration pour le serveur de passerelle.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreAdminMsg**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Met à jour le message d’administration pour le serveur de passerelle.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreConsentMsg**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Met à jour le message de consentement pour le serveur de passerelle.<br/> **Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.<br/>                                                                                                   |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGatewayServerSettings** a ces propriétés.

<dl> <dt>

**adminMessageEndTime**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de fin du message d’administration.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de début du message d’administration.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Texte du message administratif.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginCLSID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

CLSID du plug-in d’authentification actuel.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description du plug-in d’authentification actuel.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du plug-in d’authentification actuel.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginCLSID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

CLSID du plug-in d’autorisation actuel.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description du plug-in d’autorisation actuel.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du plug-in d’autorisation actuel.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**CentralCAPEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les serveurs d’accès aux services Bureau à distance centraux sont utilisés pour le contrôle de ce serveur. Cette propriété peut être modifiée en appelant la méthode [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le hachage de certificat pour la liaison HTTPs sur le port 443 dans IIS.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**consentMessageText**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Texte du message de consentement.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**EnforceChannelBinding**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la liaison de canal est appliquée pour le transport HTTP. Cette valeur de propriété peut être modifiée à l’aide de la méthode [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2012.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les paramètres IIS et RPC requis par le service de passerelle des services Bureau à distance sont configurés.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Retourne le nombre maximal de connexions autorisées via la passerelle des services Bureau à distance. Cette propriété peut être définie à l’aide de la méthode [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de connexions autorisé par l’unité de conservation des stocks (SKU).

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Retourne le nombre maximal d’événements de journal.

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de protocoles pris en charge par la passerelle des services Bureau à distance.

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si seuls les clients pouvant être autorisés à se connecter à la passerelle des services Bureau à distance sont autorisés.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

<dt>

différente
</dt> <dd>

Seuls les clients pouvant prendre en charge les messages de consentement peuvent se connecter.

</dd> <dt>

zéro
</dt> <dd>

Les clients qui ne sont pas en mesure de prendre en charge les messages peuvent également se connecter.

</dd> </dl>

</dd> <dt>

**RequestSOH**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété n’est pas prise en charge à partir de Windows Server 2016.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 et Windows Server 2008 : * *

Spécifie si le serveur doit demander une déclaration d’intégrité (SoH) au client. Cette propriété peut être modifiée à l’aide de la méthode [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la SKU.

</dd> <dt>

**SslBridging**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance. Il peut s’agir de l’une des valeurs suivantes.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

<dt>

0
</dt> <dd>

Aucun pontage SSL.

</dd> <dt>

1
</dt> <dd>

Pontage HTTPs vers HTTP.

</dd> <dt>

2
</dt> <dd>

Pontage HTTPs vers HTTPs.

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si un nombre illimité de connexions est autorisé via la passerelle des services Bureau à distance. Cette propriété peut être définie à l’aide de la méthode [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Pour utiliser cette classe, vous devez être membre du groupe administrateurs.

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

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

