---
description: Associe une instance d’une ressource allouée au pool de ressources à partir duquel elle a été allouée.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Classe Msvm_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a68731bec7ae7ab8126fa6b76305257d4333f06012e619cd7a3c9a90bcc69283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148531"
---
# <a name="msvm_elementallocatedfrompool-class"></a>MSVM \_ ElementAllocatedFromPool, classe

Associe une instance d’une ressource allouée au pool de ressources à partir duquel elle a été allouée.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ElementAllocatedFromPool** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ElementAllocatedFromPool** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **override**, **Max** (1)
</dt> </dl>

Pool de ressources. Cette propriété est héritée de la [**\_ ElementAllocatedFromPool CIM**](/previous-versions//cc150668(v=vs.85)).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Ressource allouée. Cette propriété est héritée de la [**\_ ElementAllocatedFromPool CIM**](/previous-versions//cc150668(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ElementAllocatedFromPool** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ELEMENTALLOCATEDFROMPOOL CIM**](cim-elementallocatedfrompool.md)
</dt> <dt>

[**\_ELEMENTALLOCATEDFROMPOOL CIM**](/previous-versions//cc150668(v=vs.85))
</dt> <dt>

[**MSVM \_ ElementAllocatedFromPool (v1)**](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[Classes de gestion des ressources](resource-management-classes.md)
</dt> </dl>

 

