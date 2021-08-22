---
description: Fait référence aux informations de compatibilité d’un ordinateur virtuel (en cas d’exécution sur un système informatique d’ordinateur virtuel) ou à un ordinateur hôte (lorsqu’il est exécuté sur un système d’ordinateur hôte).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Classe Msvm_CompatibilityVector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 976e6b7bd9bf69e483b987da4d8055ffc102e89c67ed83bab6aa09c4e586b1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531839"
---
# <a name="msvm_compatibilityvector-class"></a>MSVM \_ CompatibilityVector, classe

Fait référence aux informations de compatibilité d’un ordinateur virtuel (en cas d’exécution sur un système informatique d’ordinateur virtuel) ou à un ordinateur hôte (lorsqu’il est exécuté sur un système d’ordinateur hôte).

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CompatibilityVector** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CompatibilityVector** possède les propriétés suivantes.

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie l’opération de comparaison qui retourne true si et seulement si deux vecteurs sont compatibles. Les données de la machine virtuelle se trouvent sur le côté gauche de la comparaison, et les données de l’hôte se trouvent sur le côté droit.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Égal** à (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

Sur- **ensemble** (1)


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**Sous-ensemble** (2)


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

**Disjoint** (3)


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4)


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5)


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**LessThan** (6)


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7)


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**Multiple** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisible** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données d’attribut de compatibilité réelles utilisées pour la comparaison.

</dd> <dt>

**VectorId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie un vecteur de compatibilité qui représente un attribut spécifique. Cette propriété est utilisée pour faire correspondre les vecteurs correspondants entre un hôte et une machine virtuelle.

</dd> </dl>

## <a name="remarks"></a>Remarques

La méthode [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) de la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) retourne un tableau d’instances **MSVM \_ CompatibilityVector** pour l’hôte (si elle est exécutée sur l’hôte) ou une machine virtuelle (si elle est exécutée sur la machine virtuelle). Chaque entrée **MSVM \_ CompatibilityVector** de la liste décrit un vecteur d’attribut de compatibilité. Pour qu’une machine virtuelle soit compatible avec un hôte, tous ses attributs de compatibilité doivent être compatibles avec les attributs de l’hôte.

Chaque entrée **MSVM \_ CompatibilityVector** a les propriétés suivantes :

<dl> <dt>

**VectorId**
</dt> <dd>

Identifie de façon unique le vecteur de compatibilité. Il est utilisé pour faire correspondre les vecteurs à comparer entre un hôte et une machine virtuelle.

</dd> <dt>

**CompareOperation**
</dt> <dd>

Identifie l’opération de comparaison qui détermine si les vecteurs sont compatibles.

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

Contient l’attribut de compatibilité réel ; Il s’agit effectivement de la charge utile d’attribut (par exemple, masque de fonctionnalité de processeur, taille de vidage de ligne de cache, etc.).

</dd> </dl>

L’ensemble des opérations définies pour **CompareOperation** implique simplement une comparaison d’entiers de base et une logique au niveau du bit. Cela permet au contenu réel de **CompatibilityInfo** de rester opaque. L’ensemble d’opérations inclut les éléments suivants :



| CompareOperation | Description                                      | Comparaison du pseudocode                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr doit être égal à HostAttr                       | If (VmAttr = = HostAttr)              |
| VmCcSuperSet     | VmAttr doit être un sur-ensemble de HostAttr            | If ((VmAttr & HostAttr) = = HostAttr) |
| VmCcSubSet       | VmAttr doit être un sous-ensemble de HostAttr              | If ((VmAttr & HostAttr) = = VmAttr)   |
| VmCcDisjointSet  | VmAttr doit être un ensemble disjoint de HostAttr      | If ((VmAttr & HostAttr) = = 0)        |
| VmCcGreater      | VmAttr doit être supérieur à HostAttr             | If (VmAttr > HostAttr)            |
| VmCcGreaterEqual | VmAttr doit être supérieur ou égal à HostAttr | If (VmAttr >= HostAttr)           |
| VmCcLess         | VmAttr doit être inférieur à HostAttr                | If (VmAttr < HostAttr)            |
| VmCcLessEqual    | VmAttr doit être inférieur ou égal à HostAttr    | If (VmAttr <= HostAttr)           |
| VmCcMultiple     | VmAttr doit être un multiple de HostAttr            | If ((VmAttr% HostAttr) = = 0)        |
| VmCcDivisor      | VmAttr doit être un diviseur de HostAttr             | If ((HostAttr% VmAttr) = = 0)        |



 

SCVMM doit effectuer ces étapes pour déterminer si une machine virtuelle est compatible avec un ordinateur hôte.

**Pour déterminer si une machine virtuelle est compatible avec un ordinateur hôte**

1.  Itérez au sein de tous les éléments **\_ CompatibilityVector MSVM** pour la machine virtuelle.
2.  Pour chaque élément **MSVM \_ CompatibilityVector** , utilisez l’opération de compatibilité spécifiée dans **CompareOperation** pour comparer le vecteur de compatibilité matérielle des machines virtuelles avec le vecteur de compatibilité correspondant pour l’ordinateur hôte.
3.  Si tous les éléments **MSVM \_ CompatibilityVector** de la machine virtuelle sont jugés compatibles, la machine virtuelle est compatible avec l’hôte (du point de vue de la fonctionnalité de processeur).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




