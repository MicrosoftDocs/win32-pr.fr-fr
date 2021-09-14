---
description: Classe abstraite dont toutes les classes de suivi d’événements sont dérivées.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: EventTrace, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416934"
---
# <a name="eventtrace-class"></a>EventTrace, classe

Classe abstraite dont toutes les classes de suivi d’événements sont dérivées.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a>Membres

La classe **EventTrace** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **EventTrace** possède les propriétés suivantes.

<dl> <dt>

**EventGuid**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8), **Max** (16)
</dt> </dl>

GUID de classe de trace d’événements de cet événement.

</dd> <dt>

**Événements**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1)
</dt> </dl>

Nombre total d’octets de l’événement.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3)
</dt> </dl>

Type d’événement défini par le fournisseur. Indique la classe de type d’événement à utiliser pour déchiffrer les données d’événement définies par le fournisseur (les données pointées par **MofData**.

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (11)
</dt> </dl>

Identificateur de cette instance d’événement.

</dd> <dt>

**KernelTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (9)
</dt> </dl>

Durée d’exécution écoulée pour les instructions en mode noyau, en graduations de l’UC.

</dd> <dt>

**MofData**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (14), **pointeur**
</dt> </dl>

Pointeur vers les données d’événement spécifiques au fournisseur.

</dd> <dt>

**MofLength**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (15)
</dt> </dl>

Longueur des données d’événement spécifiques au fournisseur.

</dd> <dt>

**ParentGuid**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (12), **Max** (16)
</dt> </dl>

GUID de classe de trace d’événements de l’instance parente.

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (13)
</dt> </dl>

Identificateur des données de l’instance parente.

</dd> <dt>

**ReservedHeaderField**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2)
</dt> </dl>

Réservé.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6), **pointeur**
</dt> </dl>

Identifie le thread qui a généré l’événement.

</dd> <dt>

**Confirmé**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7)
</dt> </dl>

Contient la date et l’heure auxquelles l’événement s’est produit.

</dd> <dt>

**TraceLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4)
</dt> </dl>

Valeur définie par le fournisseur qui définit le niveau de gravité utilisé pour générer l’événement.

</dd> <dt>

**TraceVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5)
</dt> </dl>

Numéro de version défini par le fournisseur de la classe de trace d’événements utilisée pour générer l’événement.

</dd> <dt>

**UserTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (10)
</dt> </dl>

Durée d’exécution écoulée pour les instructions en mode utilisateur, en graduations de l’UC.

</dd> </dl>

## <a name="remarks"></a>Notes

N’utilisez pas ces propriétés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



 

 




