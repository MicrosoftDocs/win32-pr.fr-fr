---
description: Associe une instance d’une ressource allouée au nœud NUMA physique à partir duquel elle a été allouée.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Classe Msvm_ElementAllocatedFromNumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0683ba63a76d64950f48dc9787347c4f08dd433653cef3a6f0388f97420d3ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681719"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a>MSVM \_ ElementAllocatedFromNumaNode, classe

Associe une instance d’une ressource allouée au nœud NUMA physique à partir duquel elle a été allouée.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ElementAllocatedFromNumaNode** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ElementAllocatedFromNumaNode** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ NumaNode**](msvm-numanode.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Nœud NUMA physique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Ressource allouée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

