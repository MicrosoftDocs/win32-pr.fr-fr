---
description: La \_ relation SLOTINSLOT CIM représente la capacité d’un adaptateur spécial à étendre la structure d’emplacement existante afin d’activer les cartes non compatibles dans une trame ou un tableau d’hébergement.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Classe CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8163fbad7d517c936e764b51f91c77c821a33e05a6c4bdd3226246c9a27ce7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919369"
---
# <a name="cim_slotinslot-class"></a>\_Classe CIM SlotInSlot

La **relation \_ SlotInSlot CIM** représente la capacité d’un adaptateur spécial à étendre la structure d’emplacement existante afin d’activer les cartes non compatibles dans une trame ou un tableau d’hébergement. Les emplacements sont des types spéciaux de connecteurs dans lesquels les cartes d’adaptateur sont généralement insérées. L’adaptateur crée effectivement un nouvel emplacement et peut être considéré (conceptuellement) comme un emplacement dans un emplacement. Les cartes qui, autrement, seraient physiquement ou électriquement incompatibles avec les emplacements existants sont prises en charge par l’interfaçage avec l’emplacement fourni par l’adaptateur. Par exemple, les cartes réseau sont très coûteuses. À mesure que le nouveau matériel devient disponible, les configurations des châssis et des cartes changent. Pour protéger l’investissement de leurs clients, les fournisseurs de réseau fabriquent des adaptateurs spéciaux qui permettent aux anciennes cartes de s’intégrer dans de nouveaux châssis ou cartes d’hébergement ou de nouvelles cartes pour s’adapter aux anciennes cartes à l’aide d’un adaptateur spécial qui s’ajuste à un ou plusieurs emplacements existants et présente un nouvel emplacement dans lequel la carte peut s’adapter.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SlotInSlot** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SlotInSlot** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ emplacement CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Emplacement CIM**](cim-slot.md) qui décrit le ou les emplacements existants du tableau d’hébergement, ou cadre qui sont adaptés pour accueillir une carte qui, autrement, ne serait pas physiquement et/ou électriquement compatible avec celle-ci.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ emplacement CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Emplacement CIM**](cim-slot.md) qui décrit le nouvel emplacement fourni par la carte de l’adaptateur.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ SlotInSlot** est dérivée de [**CIM \_ ConnectedTo**](cim-connectedto.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CONNECTEDTO CIM**](cim-connectedto.md)
</dt> </dl>

 

