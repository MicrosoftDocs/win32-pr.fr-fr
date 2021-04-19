---
description: Représente une association entre un travail et l’élément managé responsable de la création du travail.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Classe Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534125"
---
# <a name="msvm_owningjobelement-class"></a>MSVM \_ OwningJobElement, classe

Représente une association entre un travail et l’élément managé responsable de la création du travail.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ OwningJobElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ OwningJobElement** possède les propriétés suivantes.

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Travail créé par l’élément managé.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Élément managé responsable de la création du travail.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

