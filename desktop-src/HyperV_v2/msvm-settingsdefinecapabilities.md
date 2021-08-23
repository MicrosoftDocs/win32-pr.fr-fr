---
description: Fournit un lien entre l’instance des fonctions et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Classe Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7194632af7bc1154e6a9bbca1dd5ef0bcca0fb46ab13693d20160ea404068adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950461"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>MSVM \_ SettingsDefineCapabilities, classe

Fournit un lien entre l’instance des fonctions et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SettingsDefineCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SettingsDefineCapabilities** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ fonctionnalités CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Instance des fonctionnalités. Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Paramètre utilisé pour définir l’instance des fonctions associées. Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les propriétés non null, non-clé de l’instance de données de paramètre associée sont traitées indépendamment ou comme un ensemble corrélé. Cette propriété est héritée de [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) et est toujours définie sur 0 (indépendant).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie l’instruction de prise en charge.

> [!Note]  
> cette propriété a été ajoutée dans Windows 10, version 1703.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Version préliminaire** (1)


</dt> <dd>

> [!Note]  
> Was non- **production** dans Windows 10, version 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Toute autre sémantique sur l’interprétation de toutes les propriétés non-null et non-clé des données de paramètre. Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Toute autre sémantique sur l’interprétation des propriétés non-null et non-clé des données de paramètre. Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs des propriétés **ValueRole** et **ValueRange** sont utilisées dans les paires suivantes :

-   Point/valeur par défaut (0/0)
-   Minimums/pris en charge (1/3)
-   Maximums/pris en charge (2/3)
-   Incréments/pris en charge (3/3).

« Point » signifie que chacune des propriétés sur l’objet **PartComponent** représente la plateforme par défaut.

« Minimums » et « maximums » signifient que chacune des propriétés sur l’objet **PartComponent** représente les plus petites et les plus grandes valeurs possibles pour ces propriétés prises en charge par la plateforme en fonction de la configuration actuelle de votre ordinateur.

« Incréments » indique la granularité à laquelle vous pouvez augmenter ou diminuer les paramètres.

L’accès à la classe **MSVM \_ SettingsDefineCapabilities** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGSDEFINECAPABILITIES CIM**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**MSVM \_ SettingsDefineCapabilities (v1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Classes de gestion des ressources](resource-management-classes.md)
</dt> </dl>

 

