---
description: Cette classe est la classe de type d’événement pour les événements de thread Ready. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: ReadyThread, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1b4b3d63b63e4deb9c48f9e117122f021e9d63791292e60da3cc919a6e4535e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069809"
---
# <a name="readythread-class"></a>ReadyThread, classe

Cette classe est la classe de type d’événement pour les événements de thread Ready.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>Membres

La classe **ReadyThread** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **ReadyThread** possède les propriétés suivantes.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Valeur selon laquelle la priorité est ajustée.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Raison de l’augmentation de la priorité.



| Valeur                                                                        | Signification                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ignorez l’incrément.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Appliquez l’incrément, qui va s’atténuer de façon incrémentielle à la fin de chaque Quantum.<br/>                              |
| <dl> <dt>2</dt> </dl> | Appliquez l’incrément en guise d’augmentation qui va s’atténuer dans son intégralité à Quantum (généralement pour le don prioritaire).<br/> |



 

</dd> <dt>

Indicateur
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Les indicateurs d’État possibles sont les suivants :



| Valeur                                                                          | Signification                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | Le thread a été préparé à partir du DPC (appel de procédure différé).<br/> |
| <dl> <dt>0X2</dt> </dl> | La pile du noyau est actuellement remplacée.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | L’espace d’adressage du processus est échangé.<br/>                       |



 

Notez que lorsque la pile du noyau ou l’espace d’adressage du processus est échangé, il y a un événement ReadyThread supplémentaire après la pile du noyau ou l’espace d’adressage du processus est rétabli et le thread est prêt à être distribué.

</dd> <dt>

Réservé
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

Réservé.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Identificateur de thread du thread en cours de préparation pour l’exécution.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




