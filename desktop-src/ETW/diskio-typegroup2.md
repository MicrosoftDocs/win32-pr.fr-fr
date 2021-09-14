---
description: Cette classe est la classe de type d’événement qui marque le début des événements de lecture, d’écriture et de vidage des e/s disque. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Classe DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007438"
---
# <a name="diskio_typegroup2-class"></a>E \_ TypeGroup2, classe

Cette classe est la classe de type d’événement qui marque le début des événements de lecture, d’écriture et de vidage des e/s disque.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Membres

La classe **e \_ TypeGroup2** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **e \_ TypeGroup2** possède les propriétés suivantes.

<dl> <dt>

**Paquets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**pointeur**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Paquet de requête d’e/s. Cette propriété identifie l’activité d’e/s.

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Identificateur du thread émetteur.

**Windows server 2008 R2, Windows server 2008, Windows 7 et Windows Vista :** Cette propriété n’est pas prise en charge.

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

 

 




