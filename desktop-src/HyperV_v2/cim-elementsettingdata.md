---
description: Représente une association entre un élément managé et ses données de paramètre associées. Cette Association indique également s’il s’agit d’un paramètre par défaut ou actuel.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Classe CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86f2b83c46a9b533d922991574d33a12d0a620e1559116eccc356d2b4283e486
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812276"
---
# <a name="cim_elementsettingdata-class"></a>\_Classe CIM ElementSettingData

Représente une association entre un élément managé et ses données de paramètre associées. Cette Association indique également s’il s’agit d’un paramètre par défaut ou actuel.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ElementSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ElementSettingData** possède les propriétés suivantes.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le paramètre référencé est actuellement utilisé par l’élément.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**Est actuel** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**N’est pas à jour** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le paramètre est un paramètre par défaut pour l’élément.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

**Est la valeur par défaut** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**N’est pas une valeur par défaut** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indicateur qui signale quand et à quelle fréquence appliquer le paramètre.

Par exemple, le paramètre peut être appliqué à une demande de réinitialisation, de réinitialisation et de reconfiguration. Il peut s’agir d’un paramètre permanent, ou d’un paramètre utilisé une seule fois, comme indiqué par l’indicateur. S’il s’agit d’un paramètre permanent, le paramètre est appliqué à chaque réinitialisation de l’élément managé, jusqu’à ce que cet indicateur soit réinitialisé manuellement. Toutefois, s’il s’agit d’une utilisation unique, l’indicateur est automatiquement effacé après l’application des paramètres. En outre, si cet indicateur est défini sur une valeur autre que 0 (inconnu), il est prioritaire sur une propriété **SettingData** définie sur « default ».

Si l’élément géré est un système informatique et que la valeur de cet indicateur est « est suivant », le paramètre sera effectif à la prochaine réinitialisation du système. Et, sauf si cet indicateur est modifié, il est conservé pour les réinitialisations ultérieures du système. Toutefois, si cet indicateur est défini sur « est suivant pour une utilisation unique », ce paramètre n’est utilisé qu’une seule fois et l’indicateur est réinitialisé après cette valeur sur 2 (n’est pas suivant). Ainsi, dans l’exemple ci-dessus, si le système redémarre rapidement en succession, le paramètre ne sera pas utilisé au deuxième redémarrage.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**Est suivant** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**N’est pas suivant** (2)


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**Est ensuite utilisé pour une utilisation unique** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Élément managé.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Type de données **: \_ SettingData CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Données de paramètre associées à l’élément.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

