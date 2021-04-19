---
description: Associe le \_ BootSourceSettingData MSVM au VirtualSystemSettingData MSVM global \_ .
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Classe Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536982"
---
# <a name="msvm_bootsourcecomponent-class"></a>MSVM \_ BootSourceComponent, classe

Associe [**le \_ BootSourceSettingData MSVM**](msvm-bootsourcesettingdata.md) au [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md)global. Cette classe dérive du [**\_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ BootSourceComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ BootSourceComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’élément parent dans l’Association. Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’élément enfant dans l’Association. Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).

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

[**\_Composant CIM**](cim-component.md)
</dt> <dt>

[**\_Composant CIM**](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[**MSVM \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md)
</dt> <dt>

[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

