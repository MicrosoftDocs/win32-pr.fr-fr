---
description: Cette classe est la classe de type d’événement pour les événements de fin d’opération de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Classe FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416917"
---
# <a name="fileio_opend-class"></a>FileIo ( \_ classe ouverte)

Cette classe est la classe de type d’événement pour les événements de fin d’opération de fichier.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>Membres

La classe **FileIo \_ Opened** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **FileIo \_ Opened** possède ces propriétés.

<dl> <dt>

**Argument**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Informations supplémentaires retournées par le système de fichiers pour l’opération. Par exemple, pour une demande de lecture, nombre réel d’octets qui ont été lus.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Paquet de demande d’e/s. Cette propriété identifie l’activité d’e/s qui se termine.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Valeur de retour de l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Les événements [**FileIo**](fileio.md) sont journalisés au début de l’opération. Les événements ouverts peuvent être activés séparément pour indiquer la fin de ces opérations. La IRP peut être utilisée pour mettre en corrélation les événements de début et de fin.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




