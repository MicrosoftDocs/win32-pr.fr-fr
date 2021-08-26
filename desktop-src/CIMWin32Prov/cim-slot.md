---
description: La \_ classe d’emplacement CIM représente les connecteurs dans lesquels des packages sont insérés.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: Classe CIM_Slot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 910fb4a3dcd5d3d95ef524d838781bad8331d33d71fc0af8ebd358ac9dd9588e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919459"
---
# <a name="cim_slot-class"></a>\_Classe d’emplacement CIM

La classe d' **\_ emplacement CIM** représente les connecteurs dans lesquels des packages sont insérés. Par exemple, un package physique qui est un lecteur de disque peut être inséré dans un emplacement SCA, ou une carte (une sous-classe de [ \_ PhysicalPackage CIM](cim-physicalpackage.md)) peut être insérée dans un emplacement d’extension 16, 32 ou 64 bits sur un tableau d’hébergement. Les emplacements PCI ou PCMCIA de type III sont des exemples de ces derniers.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a>Membres

La classe d' **\_ emplacement CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ emplacement CIM** possède ces propriétés.

<dl> <dt>

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

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui décrit la configuration du code confidentiel et l’utilisation des signaux d’un connecteur physique.

Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).

</dd> <dt>

**ConnectorType**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,2 ")
</dt> </dl>

Type de connecteur physique. Un tableau est spécifié pour autoriser la description des combinaisons d’informations de connecteur. Par exemple, une entrée de tableau peut spécifier RS-232, un autre DB-25 et un troisième peut définir le connecteur comme « mâle ».

Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).

<dt>

0
</dt> <dd>

Unknown

</dd> <dt>

1
</dt> <dd>

Autres

</dd> <dt>

2
</dt> <dd>

Male

</dd> <dt>

3
</dt> <dd>

Female

</dd> <dt>

4
</dt> <dd>

Protégé

</dd> <dt>

5
</dt> <dd>

Machine

</dd> <dt>

6
</dt> <dd>

Haute densité SCSI (A) (50 broches)

</dd> <dt>

7
</dt> <dd>

SCSI (A) faible densité (50 broches)

</dd> <dt>

8
</dt> <dd>

Haute densité SCSI (P) (68 broches)

</dd> <dt>

9
</dt> <dd>

SCSI SCA-I (80 broches)

</dd> <dt>

10
</dt> <dd>

SCSI SCA-II (80 broches)

</dd> <dt>

11
</dt> <dd>

Fibre Channel SCSI (DB-9, cuivre)

</dd> <dt>

12
</dt> <dd>

Fibre Channel SCSI (fibre)

</dd> <dt>

13
</dt> <dd>

SCSI Fibre Channel SCA-II (pin 40)

</dd> <dt>

14
</dt> <dd>

SCSI Fibre Channel SCA-II (20 broches)

</dd> <dt>

15
</dt> <dd>

SCSI Fibre Channel BNC

</dd> <dt>

16
</dt> <dd>

ATA 3-1/2 pouces (40 broches)

</dd> <dt>

17
</dt> <dd>

ATA 2-1/2 pouces (44 broches)

</dd> <dt>

18
</dt> <dd>

ATA-2

</dd> <dt>

19
</dt> <dd>

ATA-3

</dd> <dt>

20
</dt> <dd>

ATA/66

</dd> <dt>

21
</dt> <dd>

DB-9

</dd> <dt>

22
</dt> <dd>

DB-15

</dd> <dt>

23
</dt> <dd>

DB-25

</dd> <dt>

24
</dt> <dd>

DB-36

</dd> <dt>

25
</dt> <dd>

RS-232C

</dd> <dt>

26
</dt> <dd>

RS-422

</dd> <dt>

27
</dt> <dd>

RS-423

</dd> <dt>

28
</dt> <dd>

RS-485

</dd> <dt>

29
</dt> <dd>

RS-449

</dd> <dt>

30
</dt> <dd>

V. 35

</dd> <dt>

31
</dt> <dd>

X. 21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

BROCHES

</dd> <dt>

34
</dt> <dd>

UTP catégorie 3

</dd> <dt>

35
</dt> <dd>

UTP catégorie 4

</dd> <dt>

36
</dt> <dd>

UTP catégorie 5

</dd> <dt>

37
</dt> <dd>

ÉQUIPÉS

</dd> <dt>

38
</dt> <dd>

RJ11

</dd> <dt>

39
</dt> <dd>

RJ

</dd> <dt>

40
</dt> <dd>

MIC fibre

</dd> <dt>

41
</dt> <dd>

Apple AUI

</dd> <dt>

42
</dt> <dd>

Port Apple

</dd> <dt>

43
</dt> <dd>

PCI

</dd> <dt>

44
</dt> <dd>

ISA

</dd> <dt>

45
</dt> <dd>

EISA

</dd> <dt>

46
</dt> <dd>

VESA

</dd> <dt>

47
</dt> <dd>

PCMCIA

</dd> <dt>

48
</dt> <dd>

Type PCMCIA I

</dd> <dt>

49
</dt> <dd>

PCMCIA type II

</dd> <dt>

50
</dt> <dd>

Type PCMCIA III

</dd> <dt>

51
</dt> <dd>

Port ZV

</dd> <dt>

52
</dt> <dd>

CardBus

</dd> <dt>

53
</dt> <dd>

USB

</dd> <dt>

54
</dt> <dd>

IEEE 1394

</dd> <dt>

55
</dt> <dd>

HIPPA

</dd> <dt>

56
</dt> <dd>

HSSDC (6 broches)

</dd> <dt>

57
</dt> <dd>

GBIC

</dd> <dt>

58
</dt> <dd>

DIN

</dd> <dt>

59
</dt> <dd>

Mini-DIN

</dd> <dt>

60
</dt> <dd>

Micro-DIN

</dd> <dt>

61
</dt> <dd>

PS/2

</dd> <dt>

62
</dt> <dd>

Infrarouge

</dd> <dt>

63
</dt> <dd>

HP-HIL

</dd> <dt>

64
</dt> <dd>

Accès à. bus

</dd> <dt>

65
</dt> <dd>

NuBus

</dd> <dt>

66
</dt> <dd>

Centronics

</dd> <dt>

67
</dt> <dd>

Mini-Centronics

</dd> <dt>

68
</dt> <dd>

Type de Mini-Centronics-14

</dd> <dt>

69
</dt> <dd>

Type de Mini-Centronics-20

</dd> <dt>

70
</dt> <dd>

Type de Mini-Centronics-26

</dd> <dt>

71
</dt> <dd>

Souris bus

</dd> <dt>

72
</dt> <dd>

BUS

</dd> <dt>

73
</dt> <dd>

AGP

</dd> <dt>

74
</dt> <dd>

Bus VME

</dd> <dt>

75
</dt> <dd>

VME64

</dd> <dt>

76
</dt> <dd>

Propriétaire

</dd> <dt>

77
</dt> <dd>

Emplacement de la carte de processeur propriétaire

</dd> <dt>

78
</dt> <dd>

Emplacement de carte mémoire propriétaire

</dd> <dt>

79
</dt> <dd>

Emplacement de la carte de montage d’e/s propriétaire

</dd> <dt>

80
</dt> <dd>

PCI-66 MHZ

</dd> <dt>

81
</dt> <dd>

AGP2X

</dd> <dt>

82
</dt> <dd>

AGP4X

</dd> <dt>

83
</dt> <dd>

PC-98

</dd> <dt>

84
</dt> <dd>

PC-98-Hireso

</dd> <dt>

85 %
</dt> <dd>

PC-H98

</dd> <dt>

86
</dt> <dd>

PC-98Note

</dd> <dt>

87
</dt> <dd>

PC-98Full

</dd> <dt>

88
</dt> <dd>

SCSI SSA

</dd> <dt>

89
</dt> <dd>

Circulaire

</dd> <dt>

90
</dt> <dd>

Connecteur IDE de la carte

</dd> <dt>

91
</dt> <dd>

Connecteur de disquette sur carte

</dd> <dt>

92
</dt> <dd>

9 broches en double en ligne

</dd> <dt>

93
</dt> <dd>

25 broche en double en ligne

</dd> <dt>

94
</dt> <dd>

50 pin double Inline

</dd> <dt>

95
</dt> <dd>

68 pin double Inline

</dd> <dt>

96
</dt> <dd>

Connecteur audio sur carte

</dd> <dt>

97
</dt> <dd>

Mini-Jack

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

SBus IEEE 1396-1993 32 bits

</dd> <dt>

100
</dt> <dd>

SBus IEEE 1396-1993 64 bits

</dd> <dt>

101
</dt> <dd>

MCA

</dd> <dt>

102
</dt> <dd>

GIO

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

HIO

</dd> <dt>

105
</dt> <dd>

NGIO

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

MTRJ

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

E/s futures

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

Electrical

</dd> <dt>

113
</dt> <dd>

Optique

</dd> <dt>

114
</dt> <dd>

Ruban

</dd> <dt>

115
</dt> <dd>

GLM

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Mini SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

HSSC

</dd> <dt>

120
</dt> <dd>

VHDCI protégé (68 broches)

</dd> <dt>

121
</dt> <dd>

InfiniBand

</dd> </dl>

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

**HeightAllowed**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)
</dt> </dl>

Hauteur maximale, en pouces, d’une carte d’adaptateur pouvant être insérée dans l’emplacement.

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

**LengthAllowed**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)
</dt> </dl>

Longueur maximale, en pouces, d’une carte d’adaptateur pouvant être insérée dans l’emplacement.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Organisation qui a produit l’élément physique. Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).

Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")
</dt> </dl>

Largeur de bus maximale, en bits, des cartes d’adaptateur qui peuvent être insérées dans l’emplacement.

<dt>

<span id="8"></span>

**8** (0)


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** (1)


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** (2)


</dt> <dd></dd> <dt>

<span id="64"></span>

**64** (3)


</dt> <dd></dd> <dt>

<span id="128"></span>

**128** (4)


</dt> <dd></dd> </dl>

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

**Nombre**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro d’emplacement physique, qui peut être utilisé comme index dans une table d’emplacements système pour déterminer si l’emplacement est physiquement occupé.

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

**PurposeDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ emplacement CIM**.**SpecialPurpose**")
</dt> </dl>

Chaîne de forme libre qui décrit comment cet emplacement est physiquement unique et qui peut contenir des types de matériel spécifiques. Cette propriété n’a de sens que lorsque la propriété booléenne **SpecialPurpose** correspondante a la valeur **true**.

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

**SpecialPurpose**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ emplacement CIM**.**PurposeDescription**")
</dt> </dl>

Si la **valeur est true**, l’emplacement est physiquement unique et peut contenir des types spéciaux de matériel (par exemple, un emplacement de processeur graphique). Si la **valeur est true**, la propriété **PurposeDescription** doit spécifier la manière dont l’emplacement est unique ou le rôle de l’emplacement.

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

**SupportsHotPlug**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’emplacement prend en charge la connexion à chaud des cartes d’adaptateur.

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

**ThermalRating**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts ")
</dt> </dl>

Dissipation thermique maximale de l’emplacement, en milliwatts.

</dd> <dt>

**VccMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,9 ")
</dt> </dl>

Tension Vcc prise en charge par l’emplacement.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5 v** (3)


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

**VppMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,10 ")
</dt> </dl>

Tension VPP prise en charge par l’emplacement.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5 v** (3)


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12V** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe d' **\_ emplacement CIM** est dérivée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).

WMI n’implémente pas cette classe. Pour les classes WMI dérivées de l' **\_ emplacement CIM**, consultez [classes Win32](win32-provider.md).

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

[**\_PHYSICALCONNECTOR CIM**](cim-physicalconnector.md)
</dt> </dl>

 

