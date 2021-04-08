---
description: La \_ classe de rack CIM représente un rack (cadre physique ou boîtier) dans lequel les châssis sont stockés. En règle générale, un rack représente le boîtier. tous les composants fonctionnels sont empaquetés dans le châssis.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: Classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748236"
---
# <a name="cim_rack-class"></a>\_Classe de rack CIM

La classe de **\_ rack CIM** représente un rack (cadre physique ou boîtier) dans lequel les châssis sont stockés. En règle générale, un rack représente le boîtier. tous les composants fonctionnels sont empaquetés dans le châssis.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Membres

La classe de **\_ rack CIM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ rack CIM** présente ces méthodes.



| Méthode                                                        | Description                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-rack.md) | Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique. Non implémenté par WMI.<br/> |



 

### <a name="properties"></a>Propriétés

La classe de **\_ rack CIM** possède ces propriétés.

<dl> <dt>

**AudibleAlarm**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le cadre est équipé d’une alarme sonore.

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")
</dt> </dl>

Chaîne de forme libre qui fournit des informations si la propriété **SecurityBreach** indique qu’une violation ou un autre événement lié à la sécurité s’est produit.

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui contient des informations sur la façon dont les différents câbles sont connectés et regroupés pour le cadre. Avec de nombreuses connexions réseau, liées au stockage et aux câbles d’alimentation, la gestion des câbles peut être un défi complexe et difficile. Cette propriété de type chaîne contient des informations pour faciliter l’assembly et le service du frame.

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Courte description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CountryDesignation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ rack CIM**.**TypeOfRack**")
</dt> </dl>

Pays ou région pour lequel le rack est conçu. Les chaînes de code du pays ou de la région sont définies par la norme ISO/IEC 3166. Le type de rack est spécifié dans la propriété **TypeOfRack** .

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Profondeur**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)
</dt> </dl>

Profondeur du package physique, en pouces.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")
</dt> </dl>

Hauteur du package physique, à l’aide de l’unité de mesure « U ». Un « U » est une unité de mesure standard pour la hauteur d’un rack, ou un composant montable en rack et est égal à 1,75 pouces ou 4,445 centimètres.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le package peut être échangé à chaud. Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé. Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud. Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LockPresent**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le frame est protégé par un verrou.

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de l’organisation qui a produit l’élément physique. Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Modèle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nom par lequel l’élément physique est généralement connu.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique. Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource. Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

> [!Note]  
> Si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées comme clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .

 

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Numéro de référence attribué par l’organisation qui a produit ou fabriqué l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’élément physique est sous tension.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Bande**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global. Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression. Si l’alimentation peut être « activée » et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud. Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas d’un package de lecteur de disque inséré à l’aide de connecteurs SCA. Toutefois, cette dernière peut être permutée à chaud. L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante. La suppression de ces composants a un impact sur la fonction de l’ensemble de l’empaquetage ou est impossible en raison de l’intégration étroite du package.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> <dt>

**Remplaçables**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement. Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée. Dans ce cas, on dit que le processeur est remplaçable. Tous les composants amovibles sont remplaçables par nature.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Table globale du conteneur physique DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Indique si une violation physique du frame a été tentée, mais a échoué ou a été tentée et réussie. Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**Aucune violation** (3)


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

**Tentative de violation** (4)


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**Violation réussie** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numéro alloué par le fabricant utilisé pour identifier le rack.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")
</dt> </dl>

Chaînes de forme libre qui fournissent des explications détaillées sur les entrées dans le tableau **ServicePhilosophy** . Notez que chaque entrée du tableau est liée à l’entrée dans **ServicePhilosophy** qui se trouve dans le même index.

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

</dd> <dt>

**ServicePhilosophy**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")
</dt> </dl>

Indique si le frame est pris en service à partir du haut, de l’avant, de l’arrière ou du côté ; et s’il a des bacs coulissants ou des côtés amovibles, et si le cadre est mobile (par exemple, des rouleaux).

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Service à partir du haut** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Service à l’avant** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Service à partir de l’arrière** (4)


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**Service de la côte** (5)


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**Plateaux coulissants** (6)


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

**Côtés amovibles** (7)


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**Mobile** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Référence (SKU)**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numéro d’unité de stock pour l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

État actuel de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément. Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia. La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc. Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé. L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue. La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**TypeOfRack**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ rack CIM**.**CountryDesignation**")
</dt> </dl>

Type de rack.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**19 pouces standard** (1)


</dt> <dd>

19 pouces standard

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Étagère d’équipement** (3)


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non standard** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Version de l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’équipement comprend une alarme visible.

Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

</dd> <dt>

**Poids**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)
</dt> </dl>

Poids du package physique, en livres.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> <dt>

**Width**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)
</dt> </dl>

Largeur du package physique, en pouces.

Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ rack CIM** est dérivée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_PHYSICALFRAME CIM**](cim-physicalframe.md)
</dt> </dl>

 

