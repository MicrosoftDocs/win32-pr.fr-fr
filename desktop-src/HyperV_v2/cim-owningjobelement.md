---
description: Représente une association entre un travail et l’élément managé qui a créé le travail.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Classe CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ea0e4371246f71d125295730c19de75c59eafb08a4c081699b6b40575f27a99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694659"
---
# <a name="cim_owningjobelement-class"></a>\_Classe CIM OwningJobElement

Représente une association entre un travail et l’élément managé qui a créé le travail. Étant donné qu’un travail peut se déplacer entre les systèmes et que l’élément géré peut ne pas exister pendant toute la durée du travail, dans certains cas, cette association peut ne pas être possible ou ne peut exister que pour une partie de l’existence du travail.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ OwningJobElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ OwningJobElement** possède les propriétés suivantes.

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

Type de données **: \_ travail CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Référence au travail créé par l’élément managé.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Référence à l’élément managé qui A créé le travail.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

