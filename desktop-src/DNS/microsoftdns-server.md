---
title: Classe MicrosoftDNS_Server
description: La \_ classe de serveur MicrosoftDNS décrit un serveur DNS. Chaque instance de cette classe peut être associée à une instance du \_ cache MicrosoftDNS, une instance de MicrosoftDNS \_ RootHints et plusieurs instances de la \_ zone MicrosoftDNS.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server de la classe DNS
- MicrosoftDNS_Server de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c4a42432a11b5cde0df657ba2a9725a68d76a055fce3787bce56c10dfd227ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539269"
---
# <a name="microsoftdns_server-class"></a>\_Classe de serveur MicrosoftDNS

La classe de **\_ serveur MicrosoftDNS** décrit un serveur DNS. Chaque instance de cette classe peut être associée à une instance du [**\_ cache MicrosoftDNS**](microsoftdns-cache.md), une instance de [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)et plusieurs instances de la [**\_ zone MicrosoftDNS**](microsoftdns-zone.md).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a>Membres

La classe de **\_ serveur MicrosoftDNS** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ serveur MicrosoftDNS** possède ces méthodes.



| Méthode                   | Description                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **GetDistinguishedName** | Récupère le nom unique DNS de la zone.<br/>                        |
| **StartScavenging**      | Démarre le nettoyage des enregistrements obsolètes dans les zones soumises au nettoyage.<br/> |
| **StartService**         | Démarre le serveur DNS.<br/>                                                |
| **StopService**          | Arrête le serveur DNS.<br/>                                                 |



 

### <a name="properties"></a>Propriétés

La classe de **\_ serveur MicrosoftDNS** possède les propriétés suivantes.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre maximal d’enregistrements d’hôte renvoyés en réponse à une demande d’adresse. Les valeurs comprises entre 5 et 28 sont valides.

</dd> <dt>

**Possède**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le serveur DNS accepte les demandes de mise à jour dynamiques. Les valeurs valides sont indiquées dans le tableau suivant.



| Valeur                                                                                                | Signification                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucune restriction.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | N’autorise pas les mises à jour dynamiques des enregistrements SOA.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | N’autorise pas les mises à jour dynamiques des enregistrements NS à la racine de la zone.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | N’autorise pas les mises à jour dynamiques des enregistrements NS qui ne se trouvent pas à la racine de la zone (enregistrements NS de délégation).<br/> |



 

Additionnez ces valeurs pour déterminer la valeur du paramètre.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS tente de mettre à jour ses entrées de cache en utilisant les données des serveurs racines. Lorsqu’un serveur DNS démarre, il a besoin d’une liste de NS « indicateurs » du serveur racine et d’enregistrements A pour les serveurs historiquement appelés « fichier cache ». Les serveurs DNS Microsoft ont une fonctionnalité qui leur permet de tenter d’écrire un nouveau fichier cache en fonction des réponses des serveurs racine.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique quelles zones principales standard faisant autorité pour le nom du serveur DNS doivent être mises à jour lorsque le serveur de noms change. Les valeurs valides sont les suivantes :



| Valeur                                                                                                | Signification                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucun.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Uniquement les serveurs qui autorisent les mises à jour dynamiques.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Seuls les serveurs qui n’autorisent pas les mises à jour dynamiques.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Tous les serveurs.<br/>                                    |



 

La valeur par défaut est 1.

* * Windows Server 2003 : * *

Le nombre 3 représente tous les serveurs.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Détermine le format de message AXFR lors de l’envoi à des serveurs secondaires de serveur DNS non-Microsoft. Lorsque la valeur est TRUE, le serveur DNS envoie les transferts vers des serveurs secondaires DNS non-Microsoft au format non compressé. Si la valeur est FALSe, tous les transferts sont envoyés dans le format rapide.

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Méthode d’initialisation pour le serveur DNS. Le tableau ci-dessous répertorie les valeurs valides.



| Valeur                                                                                                | Signification                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Non initialisé.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Démarrez à partir du fichier.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Démarrage à partir du Registre.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Démarrez à partir du répertoire et du Registre.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Valeur **ScavengingInterval** par défaut définie pour toutes les zones intégrées à Active Directory créées sur ce serveur DNS. La valeur par défaut est zéro, ce qui indique que le nettoyage est désactivé.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle de non-actualisation, en heures, défini pour toutes les zones intégrées à l’Active Directory créées sur ce serveur DNS. La valeur par défaut est 168 heures (sept jours).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle d’actualisation, en heures, défini pour toutes les zones intégrées à l’Active Directory créées sur ce serveur DNS. La valeur par défaut est 168 heures (sept jours).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS crée automatiquement des zones de recherche inversée standard.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si la liaison de port par défaut pour un socket utilisé pour envoyer des requêtes à des serveurs DNS distants peut être remplacée.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il existe un DS disponible sur le serveur DNS.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle, en secondes, pour interroger les zones DS intégrées.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Durée de vie des enregistrements désactivés dans les zones intégrées du service d’annuaire, en secondes.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Durée de vie, en secondes, des informations mises en cache qui décrivent la version d’EDNS prise en charge par d’autres serveurs DNS.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la prise en charge des partitions d’annuaire d’applications est activée sur le serveur DNS.

* * Windows Server 2003 : * *

Cette méthode est nommée EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le serveur DNS comprend des enregistrements de ressource spécifiques à DNSSEC, KEY, SIG et NXT dans une réponse, conformément au tableau suivant :



| Valeur                                                                                                | Signification                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucun enregistrement DNSSEC n’est inclus dans la réponse, sauf si la requête a demandé un jeu d’enregistrements de ressources du type d’enregistrement DNSSEC.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Les enregistrements DNSSEC sont inclus dans la réponse conformément à la norme RFC 2535.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Les enregistrements DNSSEC sont inclus dans une réponse uniquement si la requête du client d’origine contenait l’enregistrement de ressource OPT conformément à la norme RFC 2671<br/> |



 

Si une requête demande un jeu d’enregistrements de ressources du type DNSSEC, le serveur DNS répond toujours avec ces enregistrements, s’ils sont disponibles.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie le comportement du serveur DNS. Si la valeur est TRUE, le serveur DNS répond toujours avec les enregistrements de ressource OPT conformément à la RFC 2671, sauf si le serveur distant a indiqué qu’il ne prend pas en charge EDNS dans un échange antérieur. Si la valeur est FALSe, le serveur DNS répond aux requêtes avec OPTs uniquement si les OPTs sont envoyées dans la requête d’origine.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique les événements que le serveur DNS enregistre dans le journal système observateur d’événements. Les valeurs suivantes sont utilisées.



| Valeur                                                                                                | Signification                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucun.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Consigner uniquement les erreurs.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Consigne uniquement les avertissements et les erreurs.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Consigner tous les événements.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si les requêtes vers les sous-zones déléguées sont transférées.

</dd> <dt>

**Redirecteurs**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Énumère la liste des adresses IP des redirecteurs sur lesquels le serveur DNS transfère des requêtes.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Durée, en secondes, pendant laquelle un serveur DNS qui transfère une requête attend la résolution du [*redirecteur*](f-gly.md) avant de tenter de résoudre lui-même la requête.

Cette valeur n’a pas de sens si le serveur de transfert n’est pas configuré pour utiliser la récursivité. Pour déterminer cela, vérifiez la propriété booléenne IsSlave.

</dd> <dt>

**IsSlave**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**True** si le serveur DNS n’utilise pas la récursivité lorsque la résolution de nom par le biais des redirecteurs échoue.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Énumère la liste des adresses IP sur lesquelles le serveur DNS peut recevoir des requêtes.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS donne la priorité à l’adresse réseau locale lors du retour d’enregistrements A.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Taille, en octets, du journal de débogage du serveur DNS.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom de fichier et chemin d’accès du journal de débogage du serveur DNS. La valeur par défaut est% System32% DNS DNS. \\ \\ log. Les chemins d’accès relatifs sont relatifs à% systemroot% \\ system32. Les chemins d’accès absolus peuvent être utilisés, mais les chemins d’accès UNC ne sont pas pris en charge.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Liste des adresses IP utilisées pour filtrer les événements DNS écrits dans le journal de débogage.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique les stratégies qui sont activées dans le journal système observateur d’événements.

Doit être défini sur des valeurs spécifiques en fonction de l’algorithme suivant : chaque stratégie (à activer dans le journal système observateur d’événements) reçoit une valeur spécifique.



| Valeur                                                                                                                  | Signification                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Demande.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Indiquer.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Mise à jour.<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Transactions qui ne sont pas des requêtes.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Questions.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Forum.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Envoi.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Réception.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | Passerelle.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Tous les paquets.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | Transaction d’écriture du service d’annuaire NT.<br/>  |
| <span id="131072"></span><dl> <dt>**131 072**</dt> </dl>         | Transaction de mise à jour du service d’annuaire NT.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Paquets complets.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Écrire.<br/>                           |



 

La somme des valeurs correspondant à toutes les stratégies à activer est indiquée dans cette propriété.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS effectue un caractère générique libre. Si la valeur est non définie ou égale à zéro, le serveur suit le comportement de caractères génériques spécifié dans la RFC DNS. Dans ce cas, un administrateur est invité à inclure les enregistrements MX pour tous les hôtes qui ne peuvent pas recevoir de messages. Si la valeur est différente de zéro, le serveur recherche le nœud générique le plus proche. dans ce cas, un administrateur doit placer les enregistrements MX à la racine de la zone et dans un nœud générique (« \* ») directement sous la racine de la zone. En outre, les administrateurs doivent placer les enregistrements MX à référence automatique sur les hôtes qui reçoivent leur propre courrier.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Durée maximale, en secondes, pendant laquelle l’enregistrement d’une requête de nom récursif peut rester dans le cache du serveur DNS. Le serveur DNS supprime les enregistrements du cache lorsque la valeur de cette entrée expire, même si la valeur du champ TTL de l’enregistrement est supérieure.

La valeur par défaut de cette propriété est 86 400 secondes (1 jour).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Durée maximale, en secondes, qu’une erreur de nom d’une requête récursive peut rester dans le cache du serveur DNS. DNS supprime les enregistrements du cache lorsque ce minuteur expire, même si le champ TTL est supérieur. La valeur par défaut est 86 400 (un jour).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet (FQDN) ou adresse IP du serveur DNS.

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique l’ensemble de caractères éligibles à utiliser dans les noms DNS. Les valeurs suivantes sont utilisées.



| Valeur                                                                                                | Signification                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | RFC strict (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Non RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multioctet (UTF8)<br/>  |



 

* * Windows Server 2003 : * *

La valeur « 2 » indique « any ».

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS effectue des recherches récursives. TRUE indique que les recherches récursives ne sont pas effectuées.

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Secondes écoulées avant une nouvelle tentative de recherche récursive. Si la propriété est non définie ou zéro, les nouvelles tentatives sont effectuées au bout de trois secondes. Les utilisateurs sont déconseillés de modifier cette propriété. Dans certaines situations, la propriété doit être modifiée. C’est le cas, par exemple, lorsque le serveur DNS contacte des serveurs distants via une liaison lente et que le serveur DNS tente une nouvelle tentative avant de recevoir la réponse du DNS distant. Dans ce cas, l’augmentation du délai d’attente doit être un peu plus long que le temps de réponse observé du DNS distant est raisonnable.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Secondes écoulées avant que le serveur DNS n’abandonne la requête récursive. Si la propriété n’est pas définie ou est égale à zéro, le serveur DNS abandonne au bout de 15 secondes. En général, le délai d’expiration de 15 secondes est suffisant pour permettre à toute réponse en suspens de revenir au serveur DNS.

Les utilisateurs sont déconseillés de modifier cette propriété. La propriété doit être modifiée lorsque le serveur DNS contacte des serveurs distants via une liaison lente, et que le serveur DNS est en mesure de rejeter les requêtes (avec défaillance du serveur \_ ) avant la réception des réponses.

Les programmes de résolution des clients renouvellent également les requêtes. une investigation minutieuse est donc nécessaire pour déterminer si les réponses distantes sont réellement associées à la requête qui a expiré. Dans ce cas, l’augmentation de la valeur du délai d’attente doit être légèrement plus longue que le temps de réponse observé du DNS distant est raisonnable.

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS arrondit Robins plusieurs enregistrements A.

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Protocole RPC ou protocoles sur lesquels l’appel RPC d’administration s’exécute. L’algorithme suivant est utilisé pour assigner une valeur spécifique :



| Valeur                                                                                                | Signification                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucun<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Canaux nommés<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | LPC<br/>         |



 

La somme des valeurs indique les protocoles utilisés.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle, en heures, entre deux opérations de nettoyage consécutives effectuées par le serveur DNS. La valeur zéro indique que le nettoyage est désactivé. La valeur par défaut est 168 heures (sept jours).

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS enregistre exclusivement les enregistrements de noms dans la même sous-arborescence que le serveur qui les a fournis.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Port sur lequel le serveur DNS envoie des requêtes UDP à d’autres serveurs. Par défaut, le serveur DNS envoie des requêtes sur un socket lié au port DNS.

Dans certains cas, il ne s’agit pas de la meilleure configuration. Un cas évident est lorsqu’un administrateur bloque le port DNS avec un pare-feu pour empêcher l’accès externe au serveur DNS, mais souhaite toujours que le serveur soit en mesure de contacter les serveurs DNS Internet pour fournir la résolution de noms pour les clients internes. Autre cas de figure : le serveur DNS prend en charge les réseaux disjoints (la propriété **DisjointNets** définie sur true identifie ce scénario). Dans ce cas, la définition de la propriété **SendOnNonDnsPort** sur une valeur différente de zéro indique au serveur DNS de se lier à un port arbitraire pour l’envoi aux serveurs DNS distants.

Si la valeur **SendOnNonDnsPort** est supérieure à 1024, le serveur DNS effectue une liaison explicite avec la valeur de port donnée. Cette option de configuration est utile lorsqu’un administrateur doit corriger le port de requête DNS à des fins de pare-feu.

* * Windows Server 2003 : * *

Si vous affectez à la propriété port d’envoi une valeur différente de zéro, le serveur DNS se lie à un port arbitraire pour l’envoi aux serveurs DNS distants.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Énumère la liste des adresses IP du serveur DNS.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le serveur DNS analyse les [*fichiers de zone*](z-gly.md) de manière stricte. Si la valeur n’est pas définie ou égale à zéro, le serveur consigne et ignore les données incorrectes dans le fichier de zone et poursuit le chargement. Si la valeur est différente de zéro, le serveur consigne et échoue sur les erreurs de fichier de zone.

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Restreint le type d’enregistrements qui peuvent être mis à jour dynamiquement sur le serveur, utilisé en plus des paramètres **AllowUpdate** sur les objets serveur et zone.

* * Windows Server 2003 : * *

0 : aucune restriction.

1 : ne pas autoriser les mises à jour dynamiques des enregistrements SOA.

2 : n’autorisez pas les mises à jour dynamiques des enregistrements NS à la racine de la zone.

4 : n’autorisez pas les mises à jour dynamiques des enregistrements NS qui ne sont pas à la racine de la zone (enregistrements NS de délégation).

Additionnez ces valeurs pour déterminer la valeur du paramètre.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version du serveur DNS.

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le serveur DNS écrit des enregistrements NS et SOA dans la section autorité en cas de réponse correcte.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Durée, en secondes, pendant laquelle le serveur DNS attend la réussite d’une connexion TCP à un serveur distant lors d’une tentative de transfert de zone.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode StartService de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Méthode StopService de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





