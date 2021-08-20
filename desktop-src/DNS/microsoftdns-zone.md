---
title: Classe MicrosoftDNS_Zone
description: La \_ classe de zone MicrosoftDNS décrit une zone DNS. Chaque instance de la \_ classe de zone MicrosoftDNS doit être affectée à un seul serveur DNS. Les zones peuvent être associées à plusieurs instances de \_ classes MicrosoftDNS Domain ou MicrosoftDNS \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone de la classe DNS
- MicrosoftDNS_Zone de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37b8c99fcd0fb70206758dd67dab8cfffe145ea2ef1aa75186b1268a7ff3b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957178"
---
# <a name="microsoftdns_zone-class"></a>\_Classe de zone MicrosoftDNS

> [!NOTE]
> Cet article contient des références au terme esclave, un terme que Microsoft n’utilise plus. Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.

> [!NOTE]
> Cet article contient des références au terme serveur maître, un terme que Microsoft n’utilise plus. Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.

La classe de **\_ zone MicrosoftDNS** décrit une zone DNS. Chaque instance de la classe de **\_ zone MicrosoftDNS** doit être affectée à un seul serveur DNS. Les zones peuvent être associées à plusieurs instances de classes [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) ou [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a>Membres

La classe de **\_ zone MicrosoftDNS** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ zone MicrosoftDNS** possède ces méthodes.



| Méthode                   | Description                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Active l’antériorité pour certains ou tous les enregistrements non NS et non SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Modifie les types de zone. <br/> Qualificateurs : implémentés<br/>                                                                                                                                         |
| **CreateZone**           | Crée une nouvelle zone. <br/> Qualificateurs : aucun.<br/>                                                                                                                                               |
| **ForceRefresh**         | Force une mise à jour de la base de données secondaire à partir du serveur DNS maître. <br/> Qualificateurs : implémentés<br/>                                                                                               |
| **GetDistinguishedName** | Obtient le nom unique du service d’annuaire pour la zone. <br/> Qualificateurs : implémentés<br/>                                                                                                                 |
| **PauseZone**            | Suspend la zone. <br/> Qualificateurs : implémentés<br/>                                                                                                                                            |
| **ReloadZone**           | Recharge la zone. <br/> Qualificateurs : implémentés<br/>                                                                                                                                           |
| **ResetSecondaries**     | Réinitialise le tableau d’adresses IP secondaire. <br/> Qualificateurs : implémentés<br/>                                                                                                                      |
| **ResumeZone**           | Reprend la zone. <br/> Qualificateurs : implémentés<br/>                                                                                                                                           |
| **UpdateFromDS**         | Force une mise à jour de la zone à partir du service d’annuaire (DS). Pour que cette méthode soit valide, le ZoneType doit être égal à 0. la zone doit effectivement être stockée dans le DS. <br/> Qualificateurs : implémentés<br/> |
| **WriteBackZone**        | Enregistre les données de zone dans son fichier de zone. <br/> Qualificateurs : implémentés, statiques<br/>                                                                                                                   |



 

### <a name="properties"></a>Propriétés

La classe de **\_ zone MicrosoftDNS** possède ces propriétés.

<dl> <dt>

**Cumulé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le comportement de vieillissement et de nettoyage de la zone. La valeur zéro indique que le nettoyage est désactivé. Lorsque le nettoyage est désactivé, les horodateurs des enregistrements de la zone ne sont pas actualisés et les enregistrements ne sont pas soumis au nettoyage. Lorsque la valeur est définie sur un, les enregistrements sont soumis au nettoyage et leurs horodateurs sont actualisés lorsque le serveur reçoit la requête de mise à jour dynamique pour les enregistrements. Pour les zones intégrées à Active Directory, cette valeur est définie sur la propriété *DefaultAgingState* du serveur DNS sur lequel la zone est créée. Pour les zones principales standard, la valeur par défaut est zéro.

</dd> <dt>

**Possède**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la zone accepte les demandes de mise à jour dynamique.

</dd> <dt>

**Créé automatiquement**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la zone est créée de façon autocrée.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’heure à laquelle le serveur peut tenter de nettoyer la zone. Même si la zone est configurée pour activer le nettoyage, le serveur DNS ne tentera pas de nettoyer cette zone avant ce moment. Cette valeur est définie sur l’heure actuelle plus l’intervalle d’actualisation de la zone chaque fois que la zone est chargée. Ce paramètre est stocké localement et n’est pas répliqué vers d’autres copies de la zone.

</dd> <dt>

**DataFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le nom du fichier de zone.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’enregistrement WINS est répliqué. Si la valeur est TRUE, la réplication des enregistrements WINS est désactivée.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si la zone est intégrée au service d’annuaire.

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le DNS utilise la récursivité lors de la résolution des noms pour la zone de transfert spécifiée. Applicable uniquement aux zones de transfert conditionnel.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la durée, en secondes, pendant laquelle un serveur DNS qui transfère une requête pour le nom sous la zone de transfert attend la résolution du redirecteur avant de tenter de résoudre la requête elle-même. Ce paramètre s’applique uniquement aux zones de transfert.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de secondes depuis le 1er janvier 1970 GMT, depuis la dernière vérification du numéro de série SOA de la zone.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de secondes depuis le 1er janvier 1970 GMT, depuis que la zone a été transférée pour la dernière fois à partir d’un serveur maître.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresses IP locales des serveurs DNS maîtres pour cette zone. Si cette valeur est définie, ces maîtres définissent le MasterServers trouvé dans Active Directory.

</dd> <dt>

**MasterServers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresses IP des serveurs DNS maîtres pour cette zone.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’intervalle de temps entre la dernière mise à jour de l’horodateur d’un enregistrement et le premier moment où l’horodatage peut être actualisé.

</dd> <dt>

**Notifier**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la zone principale notifie les bases de données secondaires de toute modification apportée à sa base de données RR. Définissez la valeur 1 pour notifier les secondaires.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes énumérant les adresses IP des serveurs DNS qui doivent être avertis des modifications apportées à cette zone.

</dd> <dt>

**En pause**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la zone est suspendue.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’intervalle d’actualisation, pendant lequel les enregistrements avec un horodatage différent de zéro sont censés être actualisés pour rester dans la zone. Les enregistrements qui n’ont pas été actualisés par l’expiration de l’intervalle d’actualisation peuvent être supprimés par le nettoyage suivant effectué par un serveur. Cette valeur ne doit jamais être inférieure à la période d’actualisation la plus longue des enregistrements inscrits dans la zone. Les valeurs trop petites peuvent entraîner la suppression d’enregistrements DNS valides. les valeurs trop volumineuses prolongent la durée de vie des enregistrements obsolètes. Cette valeur est définie sur la propriété *DefaultRefreshInterval,* du serveur DNS sur lequel la zone est créée.

</dd> <dt>

**TVA**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la zone est inversée (TRUE) ou Forward (FALSe).

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes qui énumère la liste des adresses IP des serveurs DNS autorisés à effectuer le nettoyage des enregistrements obsolètes de cette zone. Si la liste n’est pas spécifiée, tout serveur DNS principal faisant autorité pour la zone est autorisé à nettoyer la zone lorsque d’autres conditions préalables sont remplies.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes énumérant les adresses IP des serveurs DNS autorisés à recevoir cette zone via la réplication de zone.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le transfert de zone est autorisé uniquement aux serveurs secondaires désignés. Les serveurs secondaires désignés sont des serveurs DNS dont les adresses IP sont répertoriées dans SecondariesIPAddressesArray.

</dd> <dt>

**Arrêter**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la copie de la zone a expiré. Si la valeur est TRUE, la zone est expirée ou arrêtée.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette valeur booléenne indique si la zone utilise la recherche inversée NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la zone utilise les recherches WINS.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le type de la zone. Les valeurs autorisées sont :

-   Intégration DS
-   Principal
-   Secondary

* * Windows Server 2003 : * *

Valeurs supplémentaires :

-   Cache
-   Talon
-   Redirecteur

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

[**\_Domaine MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





