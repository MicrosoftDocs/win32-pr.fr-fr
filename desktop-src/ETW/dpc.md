---
description: Cette classe est la classe de type d’événement pour les événements DPC (Device Deferred Procedure Call). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862089"
---
# <a name="dpc-class"></a>DPC (classe)

Cette classe est la classe de type d’événement pour les événements DPC (Device Deferred Procedure Call).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a>Membres

La classe **DPC** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **DPC** possède ces propriétés.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), extension (« WmiTime »)
</dt> </dl>

Heure d’entrée DPC.

</dd> <dt>

**Simple**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Adresse de la routine DPC. Utilisez l’adresse avec les événements image pour Rechercher l’image qui a démarré.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces événements sont journalisés lors de la saisie d’un DPC. Vous utilisez ces événements pour surveiller et vérifier le comportement des pilotes et des composants en mode noyau. Par exemple, vous pouvez utiliser les événements DPC, ISR et image pour déterminer les composants qui consacrent trop de temps à des niveaux d’interruption élevés. Les événements DPC et ISR ont un horodatage d’entrée utilisé pour calculer la durée des routines. Les événements d’image sont lus pour construire les régions de mémoire qui mappent à certains modules. Vous pouvez utiliser le mappage pour localiser le module qui contient la routine d’interruption.

L’événement TimerDPC enregistre le moment où un DPC se déclenche à la suite d’un délai d’expiration du minuteur et les enregistrements d’événements ThreadDPC lors de l’exécution d’un thread DPC lié.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




