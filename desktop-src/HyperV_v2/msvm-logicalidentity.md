---
description: Associe deux éléments managés qui représentent différents aspects de la même entité sous-jacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Classe Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529049"
---
# <a name="msvm_logicalidentity-class"></a>MSVM \_ LogicalIdentity, classe

Associe deux éléments managés qui représentent différents aspects de la même entité sous-jacente. Cette classe dérive de [**\_ LogicalIdentity CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ LogicalIdentity** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ LogicalIdentity** possède les propriétés suivantes.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LogicalElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à un autre aspect de l’entité système.

</dd> <dt>

**SYSTEME**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LogicalElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à un aspect de l’élément logique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dt>

[**\_LOGICALIDENTITY CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

