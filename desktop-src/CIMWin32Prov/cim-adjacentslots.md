---
description: L' \_ Association CIM AdjacentSlots décrit la disposition des emplacements sur un tableau d’hébergement ou une carte d’adaptateur.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: Classe CIM_AdjacentSlots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111106"
---
# <a name="cim_adjacentslots-class"></a>\_Classe CIM AdjacentSlots

L’Association **CIM \_ AdjacentSlots** décrit la disposition des emplacements sur un tableau d’hébergement ou une carte d’adaptateur. Les informations, telles que la distance entre les emplacements et si elles sont « partagées » (si l’une d’elles est remplie, l’autre emplacement ne peut pas être utilisé), sont transmises en tant que propriétés d’association.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ AdjacentSlots** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ AdjacentSlots** possède les propriétés suivantes.

<dl> <dt>

**DistanceBetweenSlots**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)
</dt> </dl>

Distance, en pouces, entre les emplacements adjacents.

</dd> <dt>

**SharedSlots**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’un des emplacements est rempli par une carte d’adaptateur ; l’autre emplacement doit être laissé vide.

</dd> <dt>

**Emplacement**
</dt> <dd> <dl> <dt>

Type de données **: \_ emplacement CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’un des emplacements adjacents.

</dd> <dt>

**SlotB**
</dt> <dd> <dl> <dt>

Type de données **: \_ emplacement CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’emplacement adjacent « other ».

</dd> </dl>

## <a name="remarks"></a>Notes

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

[Classes CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

