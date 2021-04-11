---
description: Cette classe est la classe de type d’événement pour les événements de défaut de page. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: Classe PageFault_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203611"
---
# <a name="pagefault_typegroup1-class"></a>PageFault \_ TypeGroup1, classe

Cette classe est la classe de type d’événement pour les événements de défaut de page.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>Membres

La classe **PageFault \_ TypeGroup1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **PageFault \_ TypeGroup1** possède les propriétés suivantes.

<dl> <dt>

ProgramCounter
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Pointeur vers l’instruction en cours d’exécution.

</dd> <dt>

VirtualAddress
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Adresse virtuelle de la page qui a provoqué l’erreur de page.

</dd> </dl>

## <a name="remarks"></a>Notes

Une erreur de page se produit lorsqu’une page recherchée dans le cache mémoire est introuvable et doit être récupérée à partir d’un autre emplacement en mémoire (erreur logicielle) ou à partir d’un disque (défaillance matérielle).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




