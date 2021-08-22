---
description: Représente la classe de type d’événement pour les événements de type objet liés au début et à la fin de la collecte de données.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: ObTypeEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3659d89baa94da0c3161f7bcd6c9ff94d27efef467af8caafa70adfe1c4a7b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070050"
---
# <a name="obtypeevent-class"></a>ObTypeEvent, classe

Représente la classe de type d’événement pour les événements de type objet liés au début et à la fin de la collecte de données. Cet événement implique le mappage des valeurs d’index de type avec les noms de types.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a>Membres

La classe **ObTypeEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **ObTypeEvent** possède les propriétés suivantes.

<dl> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Type d'objet.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Réservé.

</dd> <dt>

**TypeName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Nom du type.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 




