---
description: Établit une &\# 0034 ; partie de&\# 0034 ; relation entre un système et tout élément système géré dont il est composé.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Classe Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393427"
---
# <a name="msvm_systemcomponent-class"></a>MSVM \_ SystemComponent, classe

Établit une relation « partie de » entre un système et tout élément système géré dont il est composé.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SystemComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SystemComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Élément parent dans l’Association. Cette propriété est héritée de la [**\_ SystemComponent CIM**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Élément enfant dans l’Association. Cette propriété est héritée de la [**\_ SystemComponent CIM**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

