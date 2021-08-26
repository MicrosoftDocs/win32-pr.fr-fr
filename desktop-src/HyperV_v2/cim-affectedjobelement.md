---
description: Représente une association entre un travail et les \_ objets propriété MANAGEDELEMENT CIM qui peuvent être affectés par son exécution.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: Classe CIM_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 85e801f4b7d32ecc66a9bdfd0b11c2e97a4331b73eaa66e54a4f7b30562e0fd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041719"
---
# <a name="cim_affectedjobelement-class"></a>\_Classe CIM AffectedJobElement

Représente une association entre un travail et les **objets \_ propriété ManagedElement CIM** qui peuvent être affectés par son exécution. Il n’est pas possible que le travail décrive tous les éléments affectés. L’objectif principal de cette association est de fournir des informations lorsqu’un travail requiert l’utilisation exclusive des éléments gérés affectés ou en décrivant les effets secondaires qui peuvent en résulter.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membres

La classe **CIM \_ AffectedJobElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ AffectedJobElement** possède les propriétés suivantes.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Élément managé affecté par l’exécution du travail.

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Type de données **: \_ travail CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Travail qui affecte l’élément géré.

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**OtherElementEffectsDescriptions**")
</dt> </dl>

Effet du travail sur l’élément géré.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Utilisation exclusive** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Impact sur les performances** (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Intégrité de l’élément** (4)


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Créer** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**ElementEffects**")
</dt> </dl>

Détails supplémentaires pour les valeurs « 1 » (autres) correspondantes dans le tableau **ElementEffects** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

