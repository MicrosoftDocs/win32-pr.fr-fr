---
description: La classe LogFileEventConsumer écrit des chaînes personnalisées dans un fichier journal texte lorsque des événements lui sont remis.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: LogFileEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518414"
---
# <a name="logfileeventconsumer-class"></a>LogFileEventConsumer, classe

La classe **LogFileEventConsumer** écrit des chaînes personnalisées dans un fichier journal texte lorsque des événements lui sont remis. Les chaînes sont séparées par des séquences de fin de ligne. Cette classe est l’un des consommateurs d’événements standard fournis par WMI. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a>Membres

La classe **LogFileEventConsumer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **LogFileEventConsumer** possède les propriétés suivantes.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre. WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation. Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nom du fichier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d’un fichier qui comprend le chemin d’accès auquel les entrées du journal sont ajoutées. Si le fichier n’existe pas, **LogFileEventConsumer** tente de le créer. Le consommateur échoue lorsque le chemin d’accès n’existe pas, ou lorsque l’utilisateur qui crée le consommateur ne dispose pas des autorisations d’écriture pour le fichier ou le chemin d’accès.

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le fichier journal est un fichier texte Unicode. Si la **valeur est false**, le fichier journal est un fichier texte de code multioctet. Si le fichier existe, cette propriété est ignorée et le paramètre de fichier actuel est utilisé. Par exemple, si **IsUnicode** a la **valeur false**, mais que le fichier existant est un fichier Unicode, Unicode est utilisé. Si **IsUnicode** a la **valeur true**, mais que le fichier est du code multioctet, le code multioctet est utilisé.

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

**MaximumFileSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille maximale d’un fichier journal en octets. Si le fichier primaire dépasse sa taille maximale, le contenu est déplacé vers un autre fichier et le fichier primaire est vidé. La valeur 0 (zéro) signifie qu’il n’y a aucune limite de taille. La valeur par défaut est 65 535 octets. La taille du fichier est vérifiée avant une opération d’écriture. Par conséquent, vous pouvez avoir un fichier légèrement plus grand que la limite de taille spécifiée. L’opération d’écriture suivante l’intercepte et démarre un nouveau fichier.

La liste suivante identifie la structure d’affectation de noms pour le fichier de sauvegarde :

-   Si le nom de fichier d’origine est 8,3, l’extension est remplacée par une chaîne au format « 001 », « 002 », et ainsi de suite, par le plus petit nombre plus grand que tous les nombres précédemment utilisés et choisis. Si « 999 » est utilisé, le nombre choisi est le plus petit nombre inutilisé.
-   Si le nom de fichier d’origine n’est pas 8,3, une chaîne au format « 001 », « 002 », et ainsi de suite, est ajoutée au nom de fichier.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Nom unique de ce consommateur.

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

[Modèle](using-standard-string-templates.md) de chaîne standard pour le texte d’une entrée de journal.

</dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> **LogFileEventConsumer** ne sécurise pas le fichier journal. Par conséquent, quand vous configurez le **LogFileEventConsumer**, il est important de spécifier un répertoire qui est sécurisé au niveau dont vous avez besoin.

 

La classe **LogFileEventConsumer** est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de **LogFileEventConsumer** pour créer un consommateur, consultez [écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md).

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

[Écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

