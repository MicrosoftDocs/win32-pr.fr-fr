---
description: Représente une association dans laquelle un \_ objet LOGICALELEMENT CIM représente une ressource allouée à partir d’un \_ objet ResourcePool CIM.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: Classe CIM_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aa1eb526054c665366211ec4fe3a5abdb1a001bddc098fba2c867479f23b18a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812556"
---
# <a name="cim_elementallocatedfrompool-class"></a>\_Classe CIM ElementAllocatedFromPool

Représente une association dans laquelle un [**objet \_ LogicalElement CIM**](cim-logicalelement.md) représente une ressource allouée à partir d’un objet [**\_ ResourcePool CIM**](cim-resourcepool.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ElementAllocatedFromPool** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ElementAllocatedFromPool** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ ResourcePool**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Pool de ressources.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LogicalElement**
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
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

