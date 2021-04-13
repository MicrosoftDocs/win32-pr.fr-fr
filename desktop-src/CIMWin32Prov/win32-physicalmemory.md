---
description: Représente un périphérique de mémoire physique situé sur un système informatique et disponible pour le système d’exploitation.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483960"
---
# <a name="win32_physicalmemory-class"></a>\_Classe PhysicalMemory Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ PhysicalMemory Win32** représente un périphérique de mémoire physique situé sur un système informatique et disponible pour le système d’exploitation.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PhysicalMemory** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PhysicalMemory** a ces propriétés.

<dl> <dt>

**Attributs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| attributes")
</dt> </dl>

SMBIOS-type 17-attributs. Représente le rang.

Cette valeur provient du membre **attributs** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**BankLabel**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,4 ")
</dt> </dl>

Étiquette physique sur laquelle se trouve la mémoire.

Exemples : « Bank 0 », « Bank A »

Cette valeur provient du membre du localisateur de la **Banque** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

</dd> <dt>

**Capacité**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" octets ")
</dt> </dl>

Capacité totale de la mémoire physique, en octets.

Cette valeur provient de la structure de l' **unité de mémoire** dans les informations de version SMBIOS. Pour les versions SMBIOS 2,1 à 2,6, la valeur provient du membre **Size** . Pour SMBIOS version 2.7 +, la valeur provient du membre de **taille étendue** .

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description de l’objet : chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConfiguredClockSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« SMBIOS \| type 17-vitesse d’horloge de la \| mémoire configurée »)
</dt> </dl>

Vitesse d’horloge configurée de l’appareil mémoire, en mégahertz (MHz), ou 0, si la vitesse est inconnue.

Cette valeur provient du membre de vitesse de l’horloge de la **mémoire configurée** de la structure du **périphérique de mémoire** dans les informations SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**ConfiguredVoltage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| tension configurée")
</dt> </dl>

Tension configurée pour cet appareil, en millivolts ou 0, si la tension est inconnue.

Cette valeur provient du membre **voltage configuré** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance. Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,8 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits ")
</dt> </dl>

Largeur des données de la mémoire physique (en bits). Une largeur de données de 0 (zéro) et une largeur totale de 8 (huit) indique que la mémoire est utilisée uniquement pour fournir des bits de correction d’erreur.

Cette valeur provient du membre de la **largeur des données** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description d’un objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceLocator**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| Device Locator")
</dt> </dl>

Étiquette du socket ou de la carte de circuit qui contient la mémoire.

Exemple : « SIMM 3 »

Cette valeur provient du membre **localisateur** de l’appareil de la structure de l' **unité de mémoire** dans les informations SMBIOS.

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,6 ")
</dt> </dl>

Facteur de forme d’implémentation pour la puce.

Cette valeur provient du membre **facteur de forme** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ puce CIM**](cim-chip.md).

<dt>



  (0)


</dt> <dd>

Unknown

</dd> <dt>



 (1)


</dt> <dd>

Autres

</dd> <dt>



 (2)


</dt> <dd>

PANNEAU

</dd> <dt>



 (3)


</dt> <dd>

DIP

</dd> <dt>



 (4)


</dt> <dd>

ZIP

</dd> <dt>



 (5)


</dt> <dd>

SOJ

</dd> <dt>



  (6)


</dt> <dd>

Propriétaire

</dd> <dt>



 (7)


</dt> <dd>

Barrett

</dd> <dt>



 (8)


</dt> <dd>

ESTOMPAGE

</dd> <dt>



 (9)


</dt> <dd>

TSOP

</dd> <dt>



 (10)


</dt> <dd>

PGA

</dd> <dt>



 (11)


</dt> <dd>

RIMM

</dd> <dt>



 douze


</dt> <dd>

SODIMM

</dd> <dt>



 (13)


</dt> <dd>

SRIMM

</dd> <dt>



 (14)


</dt> <dd>

SMD

</dd> <dt>



 (15)


</dt> <dd>

SSMP

</dd> <dt>



 (16)


</dt> <dd>

QFP

</dd> <dt>



 (17)


</dt> <dd>

TQFP

</dd> <dt>



 (18)


</dt> <dd>

SOIC

</dd> <dt>



 (19)


</dt> <dd>

LLC

</dd> <dt>



 (20)


</dt> <dd>

PLCC

</dd> <dt>



 (21)


</dt> <dd>

GRILLE

</dd> <dt>



 (22)


</dt> <dd>

FPBGA

</dd> <dt>



 (23)


</dt> <dd>

LGA

</dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, ce composant de média physique peut être remplacé par un autre physiquement, mais équivalent, alors que l’alimentation est appliquée dans le package qui le contient. Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud. Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.

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

**InterleaveDataDepth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| type SMBIOS 20 \| profondeur des données entrelacées")
</dt> </dl>

Entier 16 bits non signé nombre maximal de lignes consécutives de données qui sont accessibles en un seul transfert entrelacé à partir du périphérique de mémoire. Si la valeur est 0 (zéro), la mémoire n’est pas entrelacée.

</dd> <dt>

**InterleavePosition**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,7»)
</dt> </dl>

Position de la mémoire physique dans une entrelacement. Par exemple, dans une entrelacement 2:1, la valeur « 1 » indique que la mémoire est dans la position « paire ».

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

<dt>

0
</dt> <dd>

Pas entrelacé

</dd> <dt>

1
</dt> <dd>

Première position

</dd> <dt>

2
</dt> <dd>

Deuxième position

</dd> </dl>

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

Cette valeur provient du membre du **fabricant** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**MaxVoltage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| voltage maximum")
</dt> </dl>

Tension maximale de fonctionnement de cet appareil, en millivolts ou 0, si la tension est inconnue.

Cette valeur provient du membre **voltage maximal** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,9 ")
</dt> </dl>

Type de mémoire physique. Il s’agit d’une valeur CIM qui est mappée à la valeur SMBIOS. La propriété **SMBIOSMemoryType** contient le type de mémoire SMBIOS brute.

Cette valeur provient du membre de **type de mémoire** de la structure de l’unité de **mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span id="DRAM"></span><span id="dram"></span>**DRAM** (2)


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**DRAM synchrone** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**Edo** (5)


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span id="VRAM"></span><span id="vram"></span>**VRAM** (7)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span id="SRAM"></span><span id="sram"></span>**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span id="RAM"></span><span id="ram"></span>**RAM** (9)


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span id="ROM"></span><span id="rom"></span>**ROM** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span id="DDR"></span><span id="ddr"></span>**DDR** (20)


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)


</dt> <dd>

DDR2 — peut ne pas être disponible.

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)


</dt> <dd>

DDR2 (FB-DIMM) peut ne pas être disponible.

</dd> <dt>

24
</dt> <dd>

DDR3 — peut ne pas être disponible.

</dd> <dt>

25
</dt> <dd>

FBD2

</dt> <dd></dd> <dt>

<span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)

</dd> </dl>

</dd> <dt>

**MinVoltage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 20 \| voltage minimal")
</dt> </dl>

Tension minimale de fonctionnement de cet appareil, en millivolts ou 0, si la tension est inconnue.

Cette valeur provient du membre **voltage minimal** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**Modèle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Nom de l’élément physique.

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

Étiquette de l’objet. Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique. Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource. Si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété a la **valeur null** et les données de code-barres sont utilisées comme clé de classe dans la propriété de balise.

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

Cette valeur provient du membre du **numéro de référence** de la structure de l’unité de **mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**PositionInRow**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,6»)
</dt> </dl>

Position de la mémoire physique dans une ligne. Par exemple, s’il utilise des périphériques de mémoire 2 8 bits pour former une ligne de 16 bits, une valeur de 2 (deux) signifie que cette mémoire est le deuxième périphérique, 0 (zéro) est une valeur non valide pour cette propriété.

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

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

Si la **valeur est true**, un composant physique est amovible (s’il est conçu pour être pris dans et hors du conteneur physique dans lequel il est normalement trouvé, sans altérer la fonction de l’empaquetage global). Un composant peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression. Si l’alimentation peut être « activée » et que le composant a été supprimé, l’élément est alors amovible et peut être échangé à chaud. Par exemple, une puce de processeur pouvant être mise à niveau est amovible.

Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).

</dd> <dt>

**Remplaçables**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, ce composant de média physique peut être remplacé par un autre physiquement différent. Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée. Dans ce cas, on dit que le processeur est remplaçable. Tous les composants amovibles sont remplaçables par nature.

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

Numéro alloué par le fabricant pour identifier l’élément physique.

Cette valeur provient du membre du **numéro de série** de la structure de l’unité de **mémoire** dans les informations SMBIOS.

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

Numéro d’unité de conservation de stock pour l’élément physique.

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**SMBIOSMemoryType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| Memory \_ type")
</dt> </dl>

Type de mémoire SMBIOS brut. La valeur de la propriété **MemoryType** est une valeur CIM qui est mappée à la valeur SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**Vitesse**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« nanosecondes »)
</dt> </dl>

Vitesse de la mémoire physique, en nanosecondes.

Cette valeur provient du membre **Speed** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

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

Les valeurs possibles sont.

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

Identificateur unique pour le périphérique de mémoire physique représenté par une instance de **Win32 \_ PhysicalMemory**. Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

Exemple : « mémoire physique 1 »

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,7 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits ")
</dt> </dl>

Largeur totale, en bits, de la mémoire physique, y compris les bits de vérification ou de correction des erreurs. S’il n’existe aucun bit de correction des erreurs, la valeur de cette propriété doit correspondre à ce qui est spécifié pour la propriété **DataWidth** .

Cette valeur provient du membre **Width total** de la structure de l' **unité de mémoire** dans les informations SMBIOS.

Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).

</dd> <dt>

**TypeDetail**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| Detail type")
</dt> </dl>

Type de mémoire physique représenté.

Cette valeur provient du membre de **détail de type** de la structure de l’unité de **mémoire** dans les informations SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (4)


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Page rapide** (8)


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Colonne statique** (16)


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-statique** (32)


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchrone** (128)


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**Edo** (512)


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**DRAM de fenêtre** (1024)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Mémoire cache DRAM** (2048)


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non volatile** (4096)


</dt> <dd>

Non volatil

</dd> </dl>

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

La classe **Win32 \_ PhysicalMemory** est dérivée de [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

## <a name="examples"></a>Exemples

L’exemple PowerShell- [ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sur la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, notamment **Win32 \_ PhysicalMemory**, pour afficher des informations sur un système local ou distant.

L’exemple PowerShell de [rapport de serveur](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) de la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, y compris **Win32 \_ PhysicalMemory**, pour recueillir des informations sur le serveur et les publier dans un document Word.

L’exemple de code PowerShell suivant récupère des informations relatives à la mémoire physique de l’ordinateur local.


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



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

[**\_PHYSICALMEMORY CIM**](cim-physicalmemory.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
