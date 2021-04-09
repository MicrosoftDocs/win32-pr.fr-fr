---
title: Classe MSAD_ReplNeighbor
description: Représente la structure du voisin du service de \_ \_ réplication de contenu, qui contient les informations d’état de la réplication entrante pour un contexte d’appellation (NC) et une paire de serveurs sources spécifiques.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor de la classe Active Directory
- MSAD_ReplNeighbor de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942172"
---
# <a name="msad_replneighbor-class"></a>MSAD \_ ReplNeighbor, classe

Représente la structure du [**\_ \_ voisin du service**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) de réplication de contenu, qui contient les informations d’état de la réplication entrante pour un contexte d’appellation (NC) et une paire de serveurs sources spécifiques, tels que retournés par la fonction [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a>Membres

La classe **MSAD \_ ReplNeighbor** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSAD \_ ReplNeighbor** possède ces méthodes.



| Méthode                                                           | Description                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingContext**](syncnamingcontext-msad-replneighbor.md) | Synchronise un contexte d’appellation de destination avec l’une de ses sources.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSAD \_ ReplNeighbor** possède les propriétés suivantes.

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le chemin d’accès X. 500 de l’objet [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) qui correspond au transport sur lequel la réplication est effectuée. Affectez la valeur **null** pour la réplication RPC/IP.

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le GUID de l’objet de transport intersite qui correspond à la propriété **AsyncIntersiteTransportDN** .

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **\_ modifications de \_ \_ compresser les \_ changements de réplication DS** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ synchronisation planifiée du service de réplication de l’annuaire de réplication** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**Domaine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom canonique du domaine du contexte de nommage répliqué.

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **synchronisations de réplication de service d’annuaire \_ \_ \_ do do \_ scheduled \_** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur **DS \_ REPL \_ NBR \_ Full \_ Sync \_ en \_ cours** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ paquet Next Sync de \_ paquets de réplication complète** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ notification des modifications de l’annuaire de réplication des modifications** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si cette connexion représente un contrôleur de périphérique source qui a été supprimé. **True** si cette connexion représente un contrôleur de périphérique source qui a été supprimé ; Sinon, **false**. Par défaut, le service d’annuaire continue à répliquer ces connexions pendant un certain temps, après la suppression du contrôleur de domaine source.

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le code d’erreur **HRESULT** de la dernière tentative de réplication.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nombre de tentatives de réplication consécutives ayant échoué, à l’exclusion des connexions qui sont supposées échouer. Par exemple, si la propriété **IsDeletedSourceDsa** a la valeur **true**, elle est censée échouer.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le chemin d’accès X. 500 pour le contexte de nommage qui est répliqué par cette connexion.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le GUID du contexte de nommage répliqué.

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **réplication du service d’annuaire \_ n’est \_ \_ jamais \_ synchronisé** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **notification de modification du \_ numéro de réplication DS n’a \_ \_ pas \_ \_** été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nombre de tentatives de réplication consécutives ayant échoué.

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le jeu d’indicateurs qui spécifient des attributs et des options pour les données de réplication. Cette propriété peut être zéro ou une combinaison d’un ou plusieurs des indicateurs suivants.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**Service d’annuaire \_ REPL \_ NBR \_ inscriptible** (16 (0x10))


</dt> <dd>

La copie locale du contexte de nommage est accessible en écriture.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**Service d’annuaire \_ REPL \_ NBR \_ Sync \_ au \_ démarrage** (32 (0x20))


</dt> <dd>

La réplication de ce contexte d’appellation à partir de cette source est tentée lors du démarrage du serveur de destination. En règle générale, cet indicateur s’applique uniquement aux voisins intra-sites.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**Service d’annuaire \_ REPL \_ \_ do do \_ scheduled \_ syncs** (64 (0x40))


</dt> <dd>

Exécuter la réplication selon une planification. Cet indicateur est généralement défini, à moins que la planification de ce contexte de nommage ou source ne soit « jamais », autrement dit, la planification vide.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**Service d’annuaire \_ REPL \_ NBR \_ use \_ Async \_ intersite \_ transport** (128 (0x80))


</dt> <dd>

Exécuter la réplication indirectement par le biais du service de messagerie inter-sites. Cet indicateur est défini uniquement lors de la réplication sur SMTP. Cet indicateur n'est pas défini lors de la réplication sur RPC/IP inter-site.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**Service d’annuaire \_ \_ \_ \_ \_ Synchronisation bidirectionnelle REPL** (512 (0x200))


</dt> <dd>

Si cette valeur est définie, cela indique que lorsque la réplication entrante est terminée, le serveur de destination doit indiquer au serveur source de se synchroniser dans le sens inverse. Cette fonctionnalité est utilisée dans les scénarios d'accès à distance dans lesquels un seul des deux serveurs peut initier une connexion d'accès à distance. Par exemple, cette option peut être utilisée dans un siège social et une filiale, où la filiale se connecte au siège social sur Internet au moyen d’une connexion d’accès à distance à l’ISP.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**Service d’annuaire \_ L' \_ \_ objet REPL retourne les \_ \_ parents** de l’objet (2048 (0x800))


</dt> <dd>

Ce voisin est dans un état où il retourne les objets parents avant les objets enfants. Il bascule dans cet état après avoir reçu un objet enfant avant son parent.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**Service d’annuaire \_ Réplication \_ \_ complète \_ de la synchronisation \_ en \_ cours** (65536 (0x10000))


</dt> <dd>

Le serveur de destination exécute une synchronisation complète à partir du serveur source. Les synchronisations complètes n’utilisent pas les vecteurs qui créent des mises à jour (tels que les [**\_ \_ curseurs REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) pour le filtrage des mises à jour. Les synchronisations complètes ne sont pas utilisées dans le cadre du protocole de réplication par défaut.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**Service d’annuaire \_ Paquet de réplication \_ \_ complète à \_ synchronisation \_ \_ complète** (131072 (0x20000))


</dt> <dd>

Le dernier paquet de la source indiquait une modification d’un objet que le serveur de destination n’a pas encore créé. Le paquet suivant à demander demande au serveur source de placer tous les attributs de l’objet modifié dans le paquet.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**Service d’annuaire \_ REPL \_ \_ n’est jamais \_ synchronisé** (2097152 (0x200000))


</dt> <dd>

Aucune synchronisation n'a jamais été effectuée avec succès à partir de cette source.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**Service d’annuaire \_ Taux de réplication \_ \_ anticipé** (16777216 (0x1000000))


</dt> <dd>

Le moteur de réplication a temporairement cessé de traiter ce voisin afin de traiter un autre voisin de priorité plus élevée, que ce soit pour cette partition ou pour une autre partition. Le moteur de réplication reprendra le traitement de ce voisin une fois le travail de priorité plus élevée terminé.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**Service d’annuaire \_ Réplication \_ \_ Ignorer \_ les \_ notifications de modifications** (67108864 (0x4000000))


</dt> <dd>

Ce voisin est défini pour désactiver les synchronisations basées sur les notifications. Dans un site, les contrôleurs de domaine se synchronisent les uns avec les autres en fonction des notifications lorsque des modifications se produisent. Ce paramètre empêche ce voisin d’effectuer des synchronisations qui sont déclenchées par des notifications. Le voisin effectue toujours des synchronisations en fonction de sa planification, ou en réponse à des synchronisations demandées manuellement.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**Service d’annuaire \_ REPL \_ NBR \_ Disable \_ scheduled \_ Sync** (134217728 (0x8000000))


</dt> <dd>

Ce voisin est configuré de façon à ne pas effectuer de synchronisations selon sa planification. La seule façon dont ce voisin effectuera des synchronisations est en réponse aux notifications de modification ou aux synchronisations demandées manuellement.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**Service d’annuaire \_ Réplication des \_ \_ \_ changements de compression** (268435456 (0x10000000))


</dt> <dd>

Les modifications reçues de cette source doivent être compressées. La compression se produit généralement uniquement si le serveur source se trouve dans un autre site.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**Service d’annuaire \_ REPL \_ \_ n ° \_ de \_ notifications de modification** (536870912 (0x20000000))


</dt> <dd>

Aucune notification de modification ne doit être reçue à partir de cette source. Généralement défini uniquement si le serveur source se trouve dans un autre site.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**Service d’annuaire \_ \_Jeu d' \_ \_ attributs \_ partiels REPL NBR** (1073741824 (0x40000000))


</dt> <dd>

Ce voisin est dans un état où il recrée le contenu de ce réplica à cause d'une modification dans le jeu d'attributs partiel.

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’adresse DNS du contrôleur de domaine source.

> [!Note]  
> Cette chaîne contient un GUID modifié, et non le nom DNS canonique couramment utilisé.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le composant de chemin d’accès de l’objet pour le DSA qui représente le contrôleur de périphérique source. Cette chaîne est souvent similaire au nom de l’ordinateur, mais elle n’est pas toujours identique.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le chemin d’accès X. 500 pour le DSA qui représente le contrôleur de périphérique source.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’ID d’appel qui a été utilisé par le serveur source à partir de la dernière réplication.

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le GUID de l’agent de service d’annuaire (DSA) qui représente le contrôleur de domaine source (DC).

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le site qui contient le contrôleur de site source.

</dd> <dt>

**SyncOnStartup**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur **DS \_ REPL \_ NBR \_ Sync \_ au \_ démarrage** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de la dernière tentative de réplication.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de la dernière tentative de réplication réussie.

</dd> <dt>

**TwoWaySync**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ synchronisation de réplication du compte de réplication bi** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ \_ transport intersite asynchrone du service d’annuaire de réplication d’annuaire** a été défini dans la propriété **ReplicaFlags** .

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur de la propriété **USNLastObjChangeSynced** à la fin du dernier cycle de réplication effectué avec succès. Zéro si aucun cycle de réplication n’a été effectué avec succès.

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur d’attribut non [**modifiée**](/windows/desktop/ADSchema/a-usnchanged) de la dernière mise à jour d’objet qui a été reçue.

</dd> <dt>

**Inscriptible**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si l’indicateur d' **\_ \_ \_ écriture de réplication** de compte d’annuaire a été défini dans la propriété **ReplicaFlags** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\MicrosoftActiveDirectory racine<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

