---
description: Représente l’association entre un travail et les éléments managés qui peuvent être affectés par son exécution.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Classe Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515811"
---
# <a name="msvm_affectedstoragejobelement-class"></a>MSVM \_ AffectedStorageJobElement, classe

Représente l’association entre un travail et les éléments managés qui peuvent être affectés par son exécution.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ AffectedStorageJobElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ AffectedStorageJobElement** possède les propriétés suivantes.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Élément managé affecté par l’exécution du travail. Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ StorageJob**](msvm-storagejob.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. AffectingElement")
</dt> </dl>

Travail qui affecte l’élément affecté. Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Énumération qui décrit l’effet sur l’élément managé. Ce tableau correspond au tableau de propriétés **OtherElementEffectsDescriptions** , où ce dernier fournit des détails relatifs aux effets de haut niveau énumérés par cette propriété. Des détails supplémentaires sont requis si le tableau de propriétés **ElementEffects** contient la valeur 1, (other). Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Utilisation exclusive** (2)
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Impact sur les performances** (3)
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Intégrité de l’élément** (4)
</dt> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des détails sur l’effet à la position de tableau correspondante dans le tableau de propriétés **ElementEffects** . Ces informations sont requises chaque fois que l’élément correspondant dans le tableau de propriétés **ElementEffects** contient la valeur 1 (autre). Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ AffectedStorageJobElement** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_AFFECTEDJOBELEMENT CIM**](cim-affectedjobelement.md)
</dt> <dt>

[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Classes de stockage](storage-classes.md)
</dt> </dl>

 

