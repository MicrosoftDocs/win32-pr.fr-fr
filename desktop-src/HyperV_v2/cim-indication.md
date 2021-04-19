---
description: "\\_L’indication CIM est la classe de base abstraite pour toutes les notifications relatives aux modifications dans les objets de schéma et les données d’objet de schéma, les événements détectés par les fournisseurs et l’instrumentation. Les sous-classes de l' \\_ indication CIM représentent des types de notifications spécifiques."
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: Classe CIM_Indication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527859"
---
# <a name="cim_indication-class"></a>\_Classe d’indication CIM

**CIM \_ L’indication** est la classe de base abstraite pour toutes les notifications relatives aux modifications dans les objets de schéma et les données d’objet de schéma, les événements détectés par les fournisseurs et l’instrumentation. Les sous-classes de l' **\_ indication CIM** représentent des types de notifications spécifiques.

## <a name="syntax"></a>Syntaxe

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a>Membres

La classe d' **\_ indication CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ indication CIM** possède ces propriétés.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Notifications corrélées»), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ indication CIM**.**IndicationIdentifier**")
</dt> </dl>

Tableau qui contient les valeurs **IndicationIdentifier** des notifications associées à celui-ci.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Identificateur du filtre d’indication qui traite l’indication. Le service d’envoi définit cette propriété. Cette propriété est corrélée avec la propriété **Name** de l’objet **CIM \_ IndicationFilter** . La valeur de **IndicationFilterName** doit utiliser le format suivant :

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* doit inclure un nom de droits d’auteur, de marque déposée ou unique qui est détenu par l’entité commerciale propriétaire de l’objet.
-   *<OrgID>* ne doivent pas contenir de deux-points ( :)
-   *<LocalID>* identificateur unique choisi par l’entité métier propriétaire de l’objet.

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Identificateur de notification»)
</dt> </dl>

Identificateur de l’indication. Cette propriété peut être utilisée comme valeur de clé dans le tableau de propriétés **CorrelatedIndications** . Par conséquent, **IndicationIdentifier** doit être une valeur unique dans l’espace de noms de cette instance de classe.

Pour vous assurer que **IndicationIdentifier** est unique, il doit utiliser le format suivant :

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* doit inclure un nom de droits d’auteur, de marque déposée ou unique qui est détenu par l’entité commerciale propriétaire de l’objet.
-   *<OrgID>* ne doivent pas contenir de deux-points ( :)
-   *<LocalID>* identificateur unique choisi par l’entité métier propriétaire de l’objet.
-   Pour les instances définies par DMTF, *<OrgID>* doit avoir la valeur « CIM ».

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de l’indication. La propriété peut avoir la valeur **null** si l’entité qui a créé l’indication ne peut pas déterminer ces informations.

> [!Note]  
> La valeur **IndicationTime** peut être la même pour les indications générées rapidement.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

Gravité de l’indication du point de vue du notificateur lorsque **PerceivedSeverity** a la valeur « 1 » (autre).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravité perçue»)
</dt> </dl>

Gravité de l’indication du point de vue du notificateur.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd>

la gravité perçue de l’indication est inconnue ou indéterminée.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd>

Indique que la valeur de la gravité se trouve dans la propriété **OtherSeverity** .

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informations** (2)


</dt> <dd>

Les informations doivent être utilisées lors de la fourniture d’une réponse informatif.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Détérioré/AVERTISSEMENT** (3)


</dt> <dd>

Doit être utilisé pour permettre à l’utilisateur de décider si une action est nécessaire.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Mineure** (4)


</dt> <dd>

Une action est nécessaire, mais la situation n’est pas grave pour l’instant.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

Une action est nécessaire maintenant.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (6)


</dt> <dd>

L’action est nécessaire maintenant et l’étendue est large (peut-être une interruption imminente d’une ressource critique se produira-t-elle).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrécupérable/irrécupérable** (7)


</dt> <dd>

une erreur s’est produite, mais il est trop tard pour prendre une mesure corrective.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indication CIM**.**** Pas à pas»)
</dt> </dl>

Contexte de séquence de l’identificateur de séquence pour l’indication. Si un service ne prend pas en charge les identificateurs de séquence pour les indications, cette propriété doit avoir la valeur **null**. Si l’indication est redistribuée, cette propriété reste la même.

> [!Note]  
> L’identificateur de séquence pour l’indication permet à un écouteur d’identifier les indications dupliquées lorsque le service tente de réenvoyer des indications, de réorganiser les indications qui arrivent dans le désordre et de détecter les indications perdues.

 

Pour vous assurer que **SequenceContext** est unique, il doit utiliser le format suivant :

-   *indication-Service-Name* \# *CIM-service-START-ID* \# *écouteur-destination-création-heure*
-   *indication-Service-Name* est la valeur de la propriété **Name** de l’instance **CIM \_ IndicationService** qui fournit l’indication.
-   *CIM-service-START-ID* est un identificateur qui identifie de façon unique l’opération de démarrage d’un service. Par exemple, il peut s’agir d’un horodateur de l’heure de début ou d’un compteur qui augmente pour chaque démarrage ou redémarrage du service.
-   l' *écouteur-destination-Creation-Time* est un horodateur de l’heure de création de l’instance **CIM \_ ListenerDestination** représentant la destination de l’écouteur. nSince ce format n’est qu’une recommandation, les clients CIM doivent traiter la valeur comme un identificateur opaque pour le contexte de séquence et ne pas reposer sur ce format.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **sint64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indication CIM**.**SequenceContext**")
</dt> </dl>

Numéro de séquence de l’identificateur de séquence pour l’indication.

> [!Note]  
> L’identificateur de séquence pour l’indication permet à un écouteur d’identifier les indications dupliquées lorsque le service tente de réenvoyer des indications, de réorganiser les indications qui arrivent dans le désordre et de détecter les indications perdues.

 

Le numéro de séquence présente les caractéristiques suivantes :

-   Le numéro de séquence est réinitialisé à « 0 » chaque fois que la valeur **SequenceContext** change.
-   Chaque fois que la destination de l’écouteur reçoit une nouvelle indication, le numéro de séquence est augmenté de « 1 ».
-   Le numéro de séquence est renvoyé à « 0 » lorsque la plage de valeurs est dépassée.
-   Si l’indication est redistribuée, le pas à **pas reste le** même.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

