---
description: Cette classe est la classe de type d’événement pour les événements ISR (Interrupt Service routine). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973310"
---
# <a name="isr-class"></a>ISR (classe)

Cette classe est la classe de type d’événement pour les événements ISR (Interrupt Service routine).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a>Membres

La classe **ISR** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **ISR** possède ces propriétés.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), extension (« WmiTime »)
</dt> </dl>

Heure d’entrée ISR.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), pointeur
</dt> </dl>

Réservé.

</dd> <dt>

**ReturnValue**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Valeur booléenne indiquant si l’interruption a été revendiquée (a la valeur true si l’interruption a été revendiquée).

</dd> <dt>

**Simple**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Adresse de la routine ISR. Utilisez l’adresse avec les événements image pour Rechercher l’image qui a démarré.

</dd> <dt>

**Vecteur**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Vecteur issu de la table du descripteur d’interruption auquel la routine ISR est assignée.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




