---
description: Associe une instance d’une allocation de ressources à la liste de ressources partagées à partir de laquelle elle est allouée.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Classe Msvm_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8d3913f03560262309084d99ea97b44a165944d4b71acdcac17e2a39bfd44a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148202"
---
# <a name="msvm_resourceallocationfrompool-class"></a>MSVM \_ ResourceAllocationFromPool, classe

Associe une instance d’une allocation de ressources à la liste de ressources partagées à partir de laquelle elle est allouée.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ResourceAllocationFromPool** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ResourceAllocationFromPool** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **override**, **Max** (1)
</dt> </dl>

Pool de ressources. Cette propriété est héritée de la [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Allocation de ressources. Cette propriété est héritée de la [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ResourceAllocationFromPool** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_RESOURCEALLOCATIONFROMPOOL CIM**](cim-resourceallocationfrompool.md)
</dt> <dt>

[**\_RESOURCEALLOCATIONFROMPOOL CIM**](/previous-versions//cc150673(v=vs.85))
</dt> <dt>

[**MSVM \_ ResourceAllocationFromPool (v1)**](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[Classes de gestion des ressources](resource-management-classes.md)
</dt> </dl>

 

