---
description: L’inscription d’un consommateur d’événements permanent requiert une instance de la \_ \_ classe système EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Classe __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520612"
---
# <a name="__eventfilter-class"></a>\_\_EventFilter, classe

L’inscription d’un consommateur d’événements permanent requiert une instance de la classe système **\_ \_ EventFilter** .

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventFilter** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventFilter** possède ces propriétés.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée ce filtre. Windows Management Instrumentation (WMI) stocke le SID de l’utilisateur qui crée une instance de **\_ \_ EventFilter** ou le SID d’administrateur, selon le système d’exploitation. Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**EventAccess**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Descripteur de sécurité (SD) dans le langage SDDL (Security Descriptor Definition Language) qui contrôle l’accès aux événements remis au filtre. Utilisez cette propriété pour spécifier que seuls les événements dans le contexte de sécurité de comptes spécifiques peuvent être remis à ce filtre. Par exemple, un consommateur d’événements permanent peut effacer les journaux de sécurité uniquement lorsqu’un événement spécifique est généré par un utilisateur spécifique. Pour spécifier qui peut publier des événements sur ce filtre, utilisez le masque de **\_ \_ publication approprié WBEM** dans l’entrée de Access Control (ACE) pour la propriété [**\_ descripteur de sécurité**](--event.md) . Pour plus d’informations, consultez [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](wmi-security-constants.md). Pour plus d’informations et pour obtenir des exemples, consultez remplacement :[réception d’événements en toute sécurité](receiving-events-securely.md).

Vous pouvez configurer un descripteur de sécurité d’accès aux événements pour autoriser la remise d’un événement uniquement lorsque le compte système local génère l’événement. Pour plus d’informations sur la création d’un descripteur de sécurité et l’autorisation de l’accès, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).

Exemple : la chaîne SDDL suivante autorise uniquement les administrateurs à fournir des événements au filtre. Le droit requis pour fournir des événements est la **\_ publication WBEM Right \_ Publish** (x80).


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**EventNamespace**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Espace de noms de l’instance d’événement utilisée pour les abonnements entre espaces de noms.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Identificateur unique d’un filtre d’événement. Étant donné qu’un filtre d’événements est uniquement utilisé en interne par WMI, il est recommandé de définir cette propriété sur un identificateur global unique (**GUID**) converti en chaîne. Toutefois, les consommateurs peuvent utiliser n’importe quel schéma privé pour un nom de filtre, à condition qu’il n’y ait pas de conflit avec d’autres filtres.

</dd> <dt>

**Requête**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Requête d’événement WQL (Windows Management Instrumentation Query Language) qui spécifie le jeu d’événements pour la notification du consommateur et les conditions spécifiques pour la notification.

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Langue utilisée pour la requête. Étant donné que WMI prend actuellement en charge uniquement Langage de requêtes WMI (WQL) (WQL) en tant que langage de requête, cette propriété doit avoir la valeur « WQL ».

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ EventFilter** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md).

## <a name="examples"></a>Exemples

L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **\_ \_ EventFilter** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Création d’un filtre d’événements](creating-an-event-filter.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Événements d’analyse](monitoring-events.md)
</dt> <dt>

[Classes de consommateur standard](standard-consumer-classes.md)
</dt> <dt>

[Sécurisation des événements WMI](securing-wmi-events.md)
</dt> </dl>

 

