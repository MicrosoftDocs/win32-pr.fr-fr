---
description: Cette classe est la classe de type d’événement pour les événements de défaut de page matérielle. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: Classe PageFault_HardFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952322"
---
# <a name="pagefault_hardfault-class"></a>PageFault \_ HardFault, classe

Cette classe est la classe de type d’événement pour les événements de défaut de page matérielle.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a>Membres

La classe **PageFault \_ HardFault** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **PageFault \_ HardFault** possède les propriétés suivantes.

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6)
</dt> </dl>

Quantité de données lues à partir de ReadOffset pour répondre à l’erreur.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), pointeur
</dt> </dl>

Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement de [**\_ nom FileIo**](fileio-name.md) pour déterminer le nom du fichier.

</dd> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), extension (« WmiTime »)
</dt> </dl>

Horodatage de début auquel une erreur de page s’est produite.

</dd> <dt>

**ReadOffset**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), format ("x")
</dt> </dl>

Décalage de fichier à partir duquel les données ont été lues pour satisfaire l’erreur.

</dd> <dt>

**TThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), format ("x")
</dt> </dl>

Identificateur du thread qui a rencontré l’erreur de page.

</dd> <dt>

**VirtualAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), pointeur
</dt> </dl>

Adresse défaillante.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




