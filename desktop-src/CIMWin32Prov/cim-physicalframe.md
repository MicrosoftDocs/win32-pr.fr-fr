---
description: La \_ classe PHYSICALFRAME CIM est une classe parente de racks, de châssis et d’autres boîtiers de frames tels qu’ils sont définis dans les classes d’extension.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: Classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111266"
---
# <a name="cim_physicalframe-class"></a>\_Classe CIM PhysicalFrame

La **classe \_ PhysicalFrame CIM** est une classe parente de racks, de châssis et d’autres boîtiers de frames tels qu’ils sont définis dans les classes d’extension. Les propriétés telles que **VisibleAlarm** et **AudibleAlarm**, ainsi que les données relatives aux violations de sécurité, sont incluses dans cette classe parente.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
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
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ PhysicalFrame** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **CIM \_ PhysicalFrame** possède ces méthodes.



| Méthode                                                                 | Description                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-physicalframe.md) | Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique. Non implémenté par WMI.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **CIM \_ PhysicalFrame** possède les propriétés suivantes.

<dl> <dt>

**AudibleAlarm**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le cadre est équipé d’une alarme sonore.

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**SecurityBreach**")
</dt> </dl>

Chaîne de forme libre qui fournit plus d’informations si la propriété **SecurityBreach** indique qu’une violation ou un autre événement lié à la sécurité s’est produit.

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui contient des informations sur la façon dont les différents câbles sont connectés et regroupés pour le cadre. Avec de nombreuses connexions réseau, liées au stockage et aux câbles d’alimentation, la gestion des câbles peut être un défi complexe et difficile. Cette propriété de type chaîne contient des informations pour faciliter l’assembly et le service du frame.

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

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)
</dt> </dl>

Hauteur du package physique, en pouces.

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

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de l’organisation responsable de la production de l’élément physique. Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).

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

Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique. Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource. Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’élément physique est sous tension ; dans le cas contraire, elle est actuellement désactivée.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Bande**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global. Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression. Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud. Par exemple, une puce de processeur extensible est amovible.

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

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Table globale du conteneur physique DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**BreachDescription**")
</dt> </dl>

Indique si une violation physique du frame a été tentée, mais a échoué ou a été tentée et réussie.

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

Numéro alloué par le fabricant utilisé pour identifier l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServicePhilosophy**")
</dt> </dl>

Chaînes de forme libre qui fournissent des explications détaillées sur les entrées dans le tableau **ServicePhilosophy** .

> [!Note]  
> Chaque entrée de ce tableau est liée à l’entrée dans le tableau **ServicePhilosophy** qui se trouve dans le même index.

 

</dd> <dt>

**ServicePhilosophy**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServiceDescriptions**")
</dt> </dl>

Indique si le frame est pris en service à partir du haut, de l’avant, de l’arrière ou du côté ; et s’il a des bacs coulissants ou des côtés amovibles, et si le cadre est mobile (par exemple, des rouleaux).

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

État actuel de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément. Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia. La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel/l’entité, indépendamment de l’emplacement physique des armoires, des adaptateurs, etc. Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé. L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue. La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Chaîne qui indique la version de l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’équipement comprend une alarme visible.

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

La classe **CIM \_ PhysicalFrame** est dérivée de [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

WMI n’implémente pas cette classe. Pour les classes WMI dérivées de **CIM \_ PhysicalFrame**, consultez [classes Win32](win32-provider.md).

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

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> </dl>

 

