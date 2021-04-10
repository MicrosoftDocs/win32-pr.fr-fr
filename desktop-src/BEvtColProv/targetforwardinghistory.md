---
description: Historique récent des modifications apportées aux données de transfert pour un ordinateur cible.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: TargetForwardingHistory, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111655"
---
# <a name="targetforwardinghistory-class"></a>TargetForwardingHistory, classe

Historique récent des modifications apportées aux données de transfert pour un ordinateur cible.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>Membres

La classe **TargetForwardingHistory** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **TargetForwardingHistory** possède les propriétés suivantes.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informations de point de terminaison du serveur collecteur. Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* .

</dd> <dt>

**Ordinateur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nom d’ordinateur de l’ordinateur cible.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Horodateur qui indique quand la connexion a été établie pour les données de transfert.

</dd> <dt>

**Destination**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Destination des données de transfert, par exemple un nom de fichier.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Format utilisé pour générer la destination des données de transfert.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Horodateur qui indique le moment où la connexion a été déconnectée.

</dd> <dt>

**Error**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Message d’erreur qui décrit une erreur rencontrée. Cette propriété est vide si aucune erreur n’a été rencontrée.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Type de fichier qui contient les données de transfert, telles que ETL.

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informations de point de terminaison de l’ordinateur cible, dans un format lisible par l’utilisateur. Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* . Par exemple, « 127.0.0.1:50000 ».

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

**GUID** SMBIOS de l’ordinateur cible.

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Adresse MAC de l’ordinateur cible.

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Horodateur du moment où ce changement d’État a été enregistré.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | Racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur WMI du collecteur d’événements de démarrage](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

