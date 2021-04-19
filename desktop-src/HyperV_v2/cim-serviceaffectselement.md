---
description: Représente une association entre un service et un élément managé qui peut être affecté par son exécution.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Classe CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514452"
---
# <a name="cim_serviceaffectselement-class"></a>\_Classe CIM ServiceAffectsElement

Représente une association entre un service et un élément managé qui peut être affecté par son exécution.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ServiceAffectsElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ServiceAffectsElement** possède les propriétés suivantes.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Élément managé affecté par le service.

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Type de données **: \_ service CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Service qui affecte l’élément managé.

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**OtherElementEffectsDescriptions**")
</dt> </dl>

Effet sur l’élément managé. Ce tableau correspond au tableau **OtherElementEffectsDescriptions** .

\- Utilisation exclusive (2) : aucun autre service ne peut avoir cette association avec l’élément.

\- Impact sur les performances (3) : déconseillé en faveur de « consomme », « améliore les performances » ou « dégrade les performances ». L’exécution du service peut améliorer ou dégrader les performances de l’élément. Cela peut être un effet secondaire de l’exécution ou comme une conséquence prévue des méthodes fournies par le service.

\- Intégrité de l’élément (4) : déconseillé en faveur de « consomme », « améliore l’intégrité » ou « dégrade l’intégrité ». L’exécution du service peut améliorer ou dégrader l’intégrité de l’élément. Cela peut être un effet secondaire de l’exécution ou comme une conséquence prévue des méthodes fournies par le service.

\- Gère (5) : le service gère l’élément.

\- Consomme (6) : l’exécution du service consomme une partie ou la totalité de l’élément associé à la suite de l’exécution du service. Par exemple, le service peut consommer des cycles de processeur, ce qui peut affecter les performances ou le stockage qui peut affecter à la fois les performances et l’intégrité. (Par exemple, le manque de stockage gratuit peut nuire à l’intégrité en réduisant la possibilité d’enregistrer l’État. ) « Consomme » peut être utilisé seul ou conjointement avec d’autres valeurs, en particulier « diminue les performances » et « dégrade l’intégrité ».

Les « Manage » et non « consomment » doivent être utilisés pour refléter les services d’allocation qui peuvent être fournis par un service.

\- Améliore l’intégrité (7) : le service peut améliorer l’intégrité de l’élément associé.

\- Dégradation de l’intégrité (8) : le service peut nuire à l’intégrité de l’élément associé.

\- Améliore les performances (9) : le service peut améliorer les performances de l’élément associé.

\- Diminue les performances (10) : le service peut dégrader les performances de l’élément associé.

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

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**Gère** (5)


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**Consomme** (6)


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**Améliore l’intégrité** (7)


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

**Dégradation de l’intégrité** (8)


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

**Améliore les performances** (9)


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

**Dégrader les performances** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (0x8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**ElementEffects**")
</dt> </dl>

Chaque élément du tableau fournit des informations supplémentaires pour l’élément correspondant dans le tableau **ElementEffects** . Une description est requise pour tout élément du tableau **ElementEffects** ayant la valeur **other** (« 1 »).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

