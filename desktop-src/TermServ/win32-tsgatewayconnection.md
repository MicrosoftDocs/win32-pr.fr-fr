---
title: Classe Win32_TSGatewayConnection
description: Représente une connexion entre un ordinateur client et un serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection de la classe Services Bureau à distance
- Win32_TSGatewayConnection de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105832"
---
# <a name="win32_tsgatewayconnection-class"></a>\_Classe TSGatewayConnection Win32

Représente une connexion entre un ordinateur client et un serveur de passerelle Bureau à distance (passerelle Bureau à distance).

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayConnection** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayConnection** possède ces méthodes.



| Méthode                                                                     | Description                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**CheckStatus**](checkstatus-win32-tsgatewayconnection.md)               | Vérifie l’état d’une connexion au serveur de passerelle Bureau à distance et si le serveur cible est configuré pour l’équilibrage de charge.<br/> |
| [**Déconnecter**](disconnect-win32-tsgatewayconnection.md)                 | Met fin à la connexion.<br/>                                                                                                  |
| [**DisconnectProtocol**](disconnectprotocol-win32-tsgatewayconnection.md) | Met fin à toutes les connexions qui utilisent le protocole spécifié.<br/>                                                                 |
| [**DisconnectUser**](disconnectuser-win32-tsgatewayconnection.md)         | Met fin à toutes les connexions de l’utilisateur spécifié.<br/>                                                                           |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGatewayConnection** a ces propriétés.

<dl> <dt>

**ChannelId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du canal.

</dd> <dt>

**ClientAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse IP du client.

</dd> <dt>

**ConnectedPort**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Port sur la ressource connectée à laquelle l’utilisateur est connecté.

</dd> <dt>

**ConnectedResource**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur (ou du cluster) auquel le client est connecté.

</dd> <dt>

**ConnectedTime**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Horodatage du moment où la connexion a été établie. Cette heure est réinitialisée lorsque la connexion est réinitialisée, même si elle est reconnectée automatiquement.

</dd> <dt>

**ConnectionDuration**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Temps écoulé depuis l’heure de la connexion.

</dd> <dt>

**ConnectionKey**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificateur de connexion au format « tunnelId : channelID ».

</dd> <dt>

**FullUserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d’utilisateur complet de l’utilisateur connecté.

</dd> <dt>

**IdleTime**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée d’inactivité de la connexion.

</dd> <dt>

**NumberOfKilobytesReceived**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de kilo-octets reçus à partir de l’ordinateur client par le serveur de passerelle Bureau à distance.

</dd> <dt>

**NumberOfKilobytesSent**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de kilo-octets envoyés à l’ordinateur client par le serveur de passerelle Bureau à distance.

</dd> <dt>

**ProtocolName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Protocole utilisé pour se connecter au serveur de passerelle Bureau à distance.

<dt>

RDP
</dt> <dd>

Protocole du serveur de passerelle Bureau à distance.

</dd> </dl>

</dd> <dt>

**TransportProtocol**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de transport pour la connexion. Il doit s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Transport RPC sur HTTP.

</dd> <dt>

1
</dt> <dd>

Transport HTTP.

</dd> <dt>

2
</dt> <dd>

Transport UDP.

</dd> </dl>

</dd> <dt>

**TunnelId**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du tunnel.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d’utilisateur connecté au serveur de passerelle Bureau à distance.

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
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

 

