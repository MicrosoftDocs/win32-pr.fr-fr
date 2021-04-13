---
description: La \_ classe WMI OnBoardDevice WMI représente les périphériques d’adaptateur courants intégrés à la carte mère (carte système).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Classe Win32_OnBoardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201109"
---
# <a name="win32_onboarddevice-class"></a>\_Classe OnBoardDevice Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OnBoardDevice** WMI représente les périphériques d’adaptateur courants intégrés à la carte mère (carte système).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ OnBoardDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ OnBoardDevice** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance. Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 10 \| Description")
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 10 \| device type n")
</dt> </dl>

Type d’appareil représenté.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Vidéo** (3)


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

**Contrôleur SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (5)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token Ring** (6)


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

**Son** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 10 \| Device Status n")
</dt> </dl>

Si la **valeur est true**, l’appareil intégré peut être utilisé.

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, un package physique peut être échangé à chaud (s’il est possible de remplacer l’élément par un autre physiquement, mais équivalent, alors que le package qui le contient est alimenté). Par exemple, un package de lecteur de disque inséré à l’aide de connecteurs SCA est amovible et peut être échangé à chaud. Tous les packages pouvant être échangés à chaud sont par nature amovibles et remplaçables.

Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom de l’organisation responsable de la production de l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Modèle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
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

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique. Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource. Notez que si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété est **null** et les données de code-barres sont utilisées comme clé de classe dans la propriété de balise.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
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

Si la **valeur est true**, l’élément physique est sous tension.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Bande**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, un package physique est amovible (s’il est conçu pour être pris dans et hors du conteneur physique dans lequel il est normalement trouvé, sans altérer la fonction de l’empaquetage global). Un package peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression. Si l’alimentation peut être « activée » et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud. Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas d’un package de lecteur de disque inséré à l’aide de connecteurs SCA. Toutefois, cette dernière peut être permutée à chaud. L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante. La suppression de ces composants affecterait la fonction de l’ensemble de l’empaquetage ou est impossible en raison de l’intégration étroite du package.

Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).

</dd> <dt>

**Remplaçables**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, un package physique est remplaçable (s’il est possible de remplacer, d’utiliser FRU ou de mettre à niveau, l’élément avec un différent physiquement). Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée. Dans ce cas, on dit que le processeur est remplaçable. Un autre exemple est un package d’alimentation monté sur des rails coulissants. Tous les packages amovibles sont remplaçables par nature.

Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Numéro alloué par le fabricant utilisé pour identifier l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**Référence (SKU)**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
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

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

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

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificateur unique de l’appareil intégré connecté au système.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

Exemple : « on Board Device 1 »

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Version de l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ OnBoardDevice** est dérivée de [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

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

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
