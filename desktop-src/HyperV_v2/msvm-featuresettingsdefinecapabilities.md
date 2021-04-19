---
description: Fournit un lien entre l’instance des fonctionnalités du commutateur Ethernet et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Classe Msvm_FeatureSettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544697"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a>MSVM \_ FeatureSettingsDefineCapabilities, classe

Fournit un lien entre l’instance des fonctionnalités du commutateur Ethernet et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ FeatureSettingsDefineCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ FeatureSettingsDefineCapabilities** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) qui représente les fonctionnalités de la fonctionnalité de commutateur Ethernet. Cette propriété est héritée [**du \_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) qui représente les paramètres de ressource. Cette propriété est héritée [**du \_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les propriétés non **null**, non-clé de **PartComponent** sont traitées indépendamment ou comme un ensemble corrélé. Par exemple, il est possible de définir un ensemble indépendant de propriétés maximales, mais il n’existe pas de relation entre chaque propriété. D’un autre côté, il peut être nécessaire de définir plusieurs ensembles corrélés de propriétés maximum lorsque les valeurs maximales de chacune sont dépendantes de certaines d’entre elles.

Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

<dl> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Indépendant** (0)
</dt> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Corrélé** (1)
</dt> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Indique une sémantique supplémentaire sur l’interprétation de toutes les propriétés non-**null** et non-clé des données de paramètre.

Les valeurs ci-dessous sont évaluées uniquement par rapport aux propriétés numériques non **null**, non-clé, non énumérées, non-booléennes, des données de paramètre. Chaque propriété de cet ensemble doit être comparable de façon mathématique à d’autres instances de cette propriété.

Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).



| Valeur                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Point**</dt> <dt>0</dt> </dl>                     | Cette instance de données de paramètre fournit un ensemble unique de valeurs.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <dt>**Minimums**</dt> <dt>1</dt> </dl>         | Ce paramètre fournit des valeurs minimales pour les propriétés évaluées. Lorsqu’il est utilisé avec **PropertyPolicy** = « Independent », un seul paramètre de ce type doit être spécifié par instance de données de paramètre particulière pour toutes les fonctionnalités. À moins d’être restreintes par une valeur maximale sur le même jeu de propriétés, toutes les valeurs qui sont plus élevées que les valeurs spécifiées sont également considérées comme étant prises en charge par l’instance des fonctions associées. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <dt>**Maximums**</dt> <dt>2</dt> </dl>         | Ce paramètre donne des valeurs maximales pour les propriétés évaluées. Lorsqu’il est utilisé avec **PropertyPolicy** = « Independent », un seul paramètre de ce type doit être spécifié par instance de données de paramètre particulière pour toutes les fonctionnalités. À moins d’être restreintes par une valeur minimale sur le même jeu de propriétés, toutes les valeurs qui comparent les valeurs spécifiées sont également considérées comme étant prises en charge par l’instance des fonctions associées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <dt>**Incréments**</dt> <dt>3</dt> </dl> | Ce paramètre donne des valeurs d’incrément pour les propriétés évaluées. Pour les fonctionnalités associées, si une propriété évaluée n’a actuellement pas de valeurs minimales ou maximales correspondantes, la propriété n’a aucun effet. Dans le cas contraire, pour chaque propriété évaluée, sa valeur (*x*) doit être comprise entre *MinimumValue* et *MaximumValue*, et doit avoir la propriété qui, à la fois, le résultat de *MaximumValue* moins *x* et le résultat de *x* moins *MinimumValue* sont chacun un entier multiple de l' *incrément*. Si les propriétés *MinimumValue* et *MaximumValue* ne sont pas spécifiées et que l’autre est, la valeur manquante doit être respectivement considérée comme la valeur la plus basse ou la plus élevée prise en charge pour le type de données de la propriété. En outre, si un *MinimumValue* et un *MaximumValue* sont spécifiés pour une propriété évaluée, le résultat de *MaximumValue* moins *MinimumValue* doit être un entier multiple de l' *incrément*. <br/> |



 

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Spécifie une sémantique supplémentaire sur l’interprétation des propriétés non-**null** et non-clés des données de paramètre. Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).



| Valeur                                                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>0</dt> <dt>**par défaut**</dt> </dl>         | Les valeurs de propriété des données de paramètre sont utilisées comme valeurs par défaut, lors de la création d’une nouvelle instance de données de paramètre pour les éléments dont les fonctionnalités sont définies par les fonctionnalités associées. Dans les instances des données de paramètre, pour des propriétés particulières ayant le même objectif sémantique, au plus une instance de données de définition de ce type doit être spécifiée par défaut.<br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <dt>**Optimal**</dt> <dt>1</dt> </dl>         | L’instance de données de paramètre représente des valeurs de paramètre optimales pour les éléments associés aux fonctionnalités associées. Plusieurs instances de données de paramètre de composant peuvent être déclarées comme optimales.<br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <dt>**Moyenne**</dt> <dt>2</dt> </dl>                     | Les propriétés numériques non **null**, non-clé, non énumérées, non-booléennes de l’instance de données de paramètre associée représentent un point moyen sur une dimension. Pour différentes combinaisons de propriétés de définition de données, les instances de données de paramètre de plusieurs composants peuvent être déclarées comme la **moyenne**. <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <dt>**Pris en charge**</dt> <dt>3</dt> </dl> | Les propriétés non **null**, non-clés des données de paramètre représentent un ensemble de valeurs de propriétés prises en charge qui ne sont pas qualifiées autrement. <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

