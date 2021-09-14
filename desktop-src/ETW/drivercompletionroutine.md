---
description: Cette classe est la classe de type d’événement pour les événements de routine complets du pilote. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: DriverCompletionRoutine, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007427"
---
# <a name="drivercompletionroutine-class"></a>DriverCompletionRoutine, classe

Cette classe est la classe de type d’événement pour les événements de routine complets du pilote.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membres

La classe **DriverCompletionRoutine** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **DriverCompletionRoutine** possède les propriétés suivantes.

<dl> <dt>

**Paquets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Paquet de demande d’e/s.

</dd> <dt>

**Simple**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Adresse de la fonction de pilote appelée.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Identificateur qui identifie de façon unique la demande. Utilisez cet identificateur pour établir une corrélation avec les autres événements de pilote, par exemple l’événement [**DriverCompleteRequest**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**E**](diskio.md)
</dt> </dl>

 

 




