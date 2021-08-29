---
description: Association entre une instance de CIM \_ VirtualSystemSettingData et l' \_ instance VirtualSystemSettingData CIM qui représente l’instantané le plus récent sur lequel cet objet est basé.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Classe CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 2b6fa9dc11f7d5e17fbc74e24a079a56647bee37b7c0251a281b767797ab801c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244659"
---
# <a name="cim_parentchildsettingdata-class"></a>\_Classe CIM ParentChildSettingData

Association entre une instance de [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) et l’instance **\_ VirtualSystemSettingData CIM** qui représente l’instantané le plus récent sur lequel cet objet est basé.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ParentChildSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ParentChildSettingData** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’objet indépendant dans cette association.

Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Enfant**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données de paramètre pour le système virtuel qui représente l’enfant du parent.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’objet qui est dépendant de la propriété **Antecedent** .

Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données de paramètre d’instantané sur lesquelles les données de paramètres enfants sont basées.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------|
| Espace de noms<br/> | \\Cimv2 racine<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

