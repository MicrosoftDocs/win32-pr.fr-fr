---
description: 'Classe PageFault_TypeGroup1 : cette classe est la classe de type d’événement pour les événements de défaut de page. La syntaxe suivante est simplifiée à partir du code MOF.'
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
ms.openlocfilehash: 25e8c066bbaf0c66a23aba19b107c8086fac7de76e0ff2ce4873d129b8586cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151445"
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

## <a name="remarks"></a>Remarques

Une erreur de page se produit lorsqu’une page recherchée dans le cache mémoire est introuvable et doit être récupérée à partir d’un autre emplacement en mémoire (erreur logicielle) ou à partir d’un disque (défaillance matérielle).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




