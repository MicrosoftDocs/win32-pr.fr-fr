---
description: Décrit un ensemble de classes avec les propriétés et les méthodes requises, nécessaires pour gérer une entité réelle ou pour prendre en charge un scénario d’utilisation, de manière interopérable.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Classe Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0773ad1b7c992211e8bc578ac2cf2bea7706313918581ef2da9df8e2887b536d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535769"
---
# <a name="msvm_registeredprofile-class"></a>MSVM \_ RegisteredProfile, classe

Décrit un ensemble de classes avec les propriétés et les méthodes requises, nécessaires pour gérer une entité réelle ou pour prendre en charge un scénario d’utilisation, de manière interopérable.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ RegisteredProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ RegisteredProfile** possède les propriétés suivantes.

<dl> <dt>

**AdvertiseTypeDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes qui fournit des informations supplémentaires relatives à la propriété **AdvertiseType** . Une description doit être fournie lorsque le **AdvertiseType** est 1 (autre). Une entrée de ce tableau correspond au même index dans le tableau **AdvertiseTypes** . Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**AdvertiseTypes**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la publication pour les informations de profil. Il est utilisé par les services de publicité de l’infrastructure WBEM pour déterminer ce qui doit être publié, par le biais des mécanismes. La propriété est un tableau afin que le profil puisse être publié à l’aide de plusieurs mécanismes. Si cette propriété est **null**, cela équivaut à spécifier la valeur 2 (non publiée). Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Non publié** (2)
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3)
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **remplacement**
</dt> </dl>

Chaîne qui identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**OtherRegisteredOrganization**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (256)
</dt> </dl>

Chaîne qui fournit une description de l’organisation lorsque **RegisteredOrganization** contient 1 (autre). Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**RegisteredName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (256)
</dt> </dl>

Nom de ce profil inscrit. Étant donné que plusieurs versions peuvent exister pour le même **RegisteredName**, la combinaison de **RegisteredName**, **RegisteredOrganization** et **RegisteredVersion** doit identifier de façon unique le profil inscrit au sein de l’étendue de l’organisation. Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**RegisteredOrganization**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Organisation qui définit ce profil. Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium pour l’innovation des services** (4)
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**FAST** (5)
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**GGF** (6)
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**INTAP** (7)
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9)
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10-Nord-Ouest de l’efficacité énergétique** (10)
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**SNIA** (11)
</dt> <dt>

<span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Forum TM** (12)
</dt> <dt>

<span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Groupe ouvert** (13)
</dt> <dt>

<span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)
</dt> <dt>

<span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)
</dt> <dt>

<span id="IETF"></span><span id="ietf"></span>**IETF** (16)
</dt> <dt>

<span id="INCITS"></span><span id="incits"></span>**INCITS** (17)
</dt> <dt>

<span id="ISO"></span><span id="iso"></span>**ISO** (18)
</dt> <dt>

<span id="W3C"></span><span id="w3c"></span>**W3C** (19)
</dt> <dt>

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Quadrillage vert** (21)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (.. )
</dt> </dl>

</dd> <dt>

**RegisteredVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de ce profil. La chaîne doit se présenter sous la forme : "*M*. *N*. *U*» où :

-   *M* est la version principale (au format numérique) décrivant la création ou la dernière modification du profil.
-   *N* est la version mineure (au format numérique) décrivant la création ou la dernière modification du profil.
-   *U* est la mise à jour (au format numérique) décrivant la création ou la dernière modification du profil.

Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Interop racine<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

