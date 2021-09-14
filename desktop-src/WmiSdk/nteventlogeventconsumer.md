---
description: La classe NTEventLogEventConsumer journalise un message spécifique dans le journal des événements du système d’exploitation lorsqu’un événement lui est remis.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: NTEventLogEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008251"
---
# <a name="nteventlogeventconsumer-class"></a>NTEventLogEventConsumer, classe

La classe **NTEventLogEventConsumer** journalise un message spécifique dans le journal des événements du système d’exploitation lorsqu’un événement lui est remis. Cette classe est l’un des consommateurs d’événements standard fournis par WMI. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>Membres

La classe **NTEventLogEventConsumer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **NTEventLogEventConsumer** possède les propriétés suivantes.

<dl> <dt>

**Catégorie**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Catégorie d’événement. Il s’agit d’informations spécifiques à la source qui peuvent avoir n’importe quelle valeur.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre. WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation. Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Message d’événement dans la DLL du message. Cette propriété ne peut pas être **null**.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’événement. Ce paramètre peut avoir l’une des valeurs répertoriées dans la liste suivante, qui sont définies dans Winnt. h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Journal des événements \_ Opération réussie** (0 (0x0))


</dt> <dd>

Événement de réussite

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Journal des événements \_ ERREUR \_ TPYE** (1 (0x1))


</dt> <dd>

Événement d’erreur

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Journal des événements \_ \_Type d’avertissement** (2 (0X2))


</dt> <dd>

Événement d’avertissement

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Journal des événements \_ \_Type d’informations** (4 (0x4))


</dt> <dd>

Événement d’information

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Journal des événements \_ \_Succès de l’audit** (8 (0x8))


</dt> <dd>

Type d’audit de réussite

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Journal des événements \_ \_Échec de l’audit** (16 (0x10))


</dt> <dd>

Type d’audit d’échec

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de modèles de chaîne standard utilisé comme chaîne d’insertion pour un enregistrement de journal des événements.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

File d’attente maximale pour un consommateur spécifique, en octets.

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](key-qualifier.md)
</dt> </dl>

Nom unique d’un consommateur.

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la propriété d’événement qui contient les données à passer au paramètre *lpRawData* de la fonction [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la propriété d’événement qui contient un identificateur de sécurité (SID) à passer au paramètre *lpUserSid* de la fonction [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) . La propriété doit être un tableau d’octets (**UInt8**) ou une chaîne. S’il s’agit d’un tableau d’octets, il est supposé être un SID. S’il s’agit d’une chaîne, il s’agit d’un SID de chaîne converti en SID.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’éléments dans le tableau **InsertionStringTemplates** .

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la source où se trouve un message. Le client est supposé avoir inscrit une DLL avec les messages nécessaires.

> [!Note]  
> La valeur de ce paramètre ne doit pas inclure un signe deux-points ( :) symbole.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur sur lequel enregistrer un événement, ou **null** si l’événement doit être enregistré sur un serveur local.

Les utilisateurs authentifiés ne peuvent pas, par défaut, consigner les événements dans le journal des applications sur un ordinateur distant. Par conséquent, l’utilisation de cette propriété pour spécifier un ordinateur distant ne fonctionnera pas. Pour savoir comment modifier la sécurité du journal des événements, consultez cet article de la [base de connaissances](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **NTEventLogEventConsumer** est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de **NTEventLogEventConsumer** pour créer un consommateur, consultez [journalisation dans le journal des événements NT basé sur un événement](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Abonnement racine<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de consommateur standard](standard-consumer-classes.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

