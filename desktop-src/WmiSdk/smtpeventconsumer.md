---
description: La classe SMTPEventConsumer envoie un message électronique à l’aide du protocole SMTP (Simple Mail Transfer Protocol) chaque fois qu’un événement lui est remis.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: SMTPEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210554"
---
# <a name="smtpeventconsumer-class"></a>SMTPEventConsumer, classe

La classe **SMTPEventConsumer** envoie un message électronique à l’aide du protocole SMTP (Simple Mail Transfer Protocol) chaque fois qu’un événement lui est remis. Un serveur SMTP doit exister sur le réseau. La classe SMTPEventConsumer ne prend pas en charge les pièces jointes. L’encodage du message électronique doit être US-ASCII.

Cette classe est l’un des consommateurs d’événements standard fournis par WMI. Pour obtenir un exemple d’utilisation de **SMTPEventConsumer** pour créer un consommateur, consultez [envoi de courriers électroniques en fonction d’un événement](sending-e-mail-based-on-an-event.md). Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a>Membres

La classe **SMTPEventConsumer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SMTPEventConsumer** possède les propriétés suivantes.

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste d’adresses, séparées par une virgule ou un point-virgule, au format d’un modèle de chaîne standard auquel le message est envoyé en tant que copie carbone invisible. Pour plus d’informations, consultez la section Notes de cette rubrique.

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste d’adresses, séparées par une virgule ou un point-virgule, dans le format d’un modèle de chaîne standard auquel le message est envoyé sous la forme d’une copie carbone. Pour plus d’informations, consultez la section Notes de cette rubrique.

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

**FromLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

À partir de la ligne d’un message électronique au format d’un modèle de chaîne standard. Si la **valeur est null**, une ligne de est construite sous la forme « winmgmt@*MachineName*».

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de champs d’en-tête insérés dans un message électronique sans interprétation.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.

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

**Message**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Modèle de chaîne standard qui contient le corps d’un message électronique.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](key-qualifier.md)
</dt> </dl>

Identificateur unique pour le consommateur d’événements.

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Ligne de réponse d’un message électronique au format d’un modèle de chaîne standard. Si la **valeur est null**, aucune ligne reply-to n’est utilisée.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du serveur SMTP par le biais duquel un courrier électronique est envoyé. Les noms autorisés sont une adresse IP ou un nom DNS ou NetBIOS. Cette propriété ne peut pas être **null**.

</dd> <dt>

**Subject**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Modèle de chaîne standard qui contient l’objet d’un message électronique.

</dd> <dt>

**ToLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste d’adresses, séparées par une virgule ou un point-virgule, dans le format d’un modèle de chaîne standard qui identifie l’emplacement où le message doit être envoyé. Pour plus d’informations, consultez la section Notes de cette rubrique.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe SMTPEventConsumer est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .

Certaines propriétés **ToLine**, **CcLine** ou **BccLine** peuvent avoir la **valeur null**, mais elles ne peuvent pas toutes avoir la **valeur null**.

La réception d’un code de retour d’erreur à partir du service SMTP est considérée comme un échec.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de **SMTPEventConsumer** pour créer un consommateur, consultez [envoi de courriers électroniques en fonction d’un événement](sending-e-mail-based-on-an-event.md). Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Abonnement racine<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[Classes de consommateur standard](standard-consumer-classes.md)
</dt> <dt>

[Envoi de courrier électronique à partir d’un événement](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> </dl>

 

 




