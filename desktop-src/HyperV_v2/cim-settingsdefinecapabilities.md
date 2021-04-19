---
description: Représente une association entre les propriétés d’une \_ instance de la SETTINGDATA CIM et une \_ instance des fonctionnalités CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: Classe CIM_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521055"
---
# <a name="cim_settingsdefinecapabilities-class"></a>\_Classe CIM SettingsDefineCapabilities

Représente une association entre les propriétés d’une instance de la [**\_ SettingData CIM**](cim-settingdata.md) et une instance des [**\_ fonctionnalités CIM**](cim-capabilities.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SettingsDefineCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SettingsDefineCapabilities** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ fonctionnalités CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Référence à l’instance [**des \_ fonctionnalités CIM**](cim-capabilities.md) .

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ SettingData CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Référence à l’instance [**du \_ SettingData CIM**](cim-settingdata.md) utilisée pour définir l’instance des [**\_ fonctionnalités CIM**](cim-capabilities.md) .

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Indique si les propriétés non null, non-clé de l’instance du [**\_ SettingData CIM**](cim-settingdata.md) associée sont traitées indépendamment ou comme un ensemble corrélé. Par exemple, un ensemble indépendant de propriétés maximales peut être défini lorsqu’il n’existe aucune relation entre chaque propriété. En revanche, il peut être nécessaire de définir plusieurs ensembles corrélés de propriétés maximum lorsque les valeurs maximales de chacune sont dépendantes de certaines d’entre elles.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Indépendant** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Corrélé** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRole**")
</dt> </dl>

Indique le type de plage de valeurs utilisé par les propriétés des propriétés non-null et non-clé de l’instance du [**\_ SettingData CIM**](cim-settingdata.md) .

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Point** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Valeurs minimales** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Valeurs maximales** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Incréments** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Sémantique supplémentaire pour l’interprétation des propriétés non-null et non-clé de l’instance de la [**\_ SettingData CIM**](cim-settingdata.md) .

« Default » indique que les valeurs de propriété de l’instance de l’SettingData du composant seront utilisées comme valeurs par défaut, lorsqu’une nouvelle instance SettingData est créée pour les éléments dont les fonctionnalités sont définies par l’instance des fonctions associées.

Dans les instances de SettingData, pour des propriétés particulières ayant le même objectif sémantique, au plus une de ces instances SettingData sera spécifiée comme valeur par défaut.

« Optimal » indique que l’instance de SettingData représente des valeurs de paramètre optimales pour les éléments associés à l’instance des fonctions associées. Plusieurs instances de SettingData de composant peuvent être déclarées comme optimales.» Mean» indique que les propriétés numériques non-null, non-clé, non énumérées, non-booléennes de l’instance SettingData associée représentent un point moyen sur une dimension. Pour différentes combinaisons de propriétés SettingData, plusieurs instances de SettingData de composant peuvent être déclarées comme « moyennes ». « Pris en charge » indique que les propriétés non null, non-clé de l’instance de l’élément SettingData du composant représentent un ensemble de valeurs de propriétés prises en charge qui ne sont pas qualifiées autrement.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valeur par défaut** (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Optimal** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Moyenne** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Pris en charge** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Composant CIM**](cim-component.md)
</dt> </dl>

 

