---
description: Cette classe est la classe de type d’événement pour les événements de vidage d’e/s de disque. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: Classe DiskIo_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e421a8bd596869ac06af61f05ed1af8c633fb23b95e576398de6418620249c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050659"
---
# <a name="diskio_typegroup3-class"></a>E \_ TypeGroup3, classe

Cette classe est la classe de type d’événement pour les événements de vidage d’e/s de disque.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Membres

La classe **e \_ TypeGroup3** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **e \_ TypeGroup3** possède les propriétés suivantes.

<dl> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Numéro qui identifie le disque physique.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération.

</dd> <dt>

**Paquets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**pointeur**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Paquet de requête d’e/s. Cette propriété identifie l’activité d’e/s.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Peut contenir un ou plusieurs des indicateurs de paquets de requêtes d’e/s suivants (définis dans Ntddk. h, qui est un fichier d’en-tête DDK) :

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOcache**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **\_ \_ e/s de pagination IRP**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **\_achèvement du montage IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **API de l’IRP \_ synchrone \_**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **\_IRP associée de la IRP \_**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **\_e/s mises en mémoire tampon IRP \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**\_mémoire tampon d’IRP DEALLOCATE \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **\_opération d’entrée IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **\_ \_ e/s de pagination synchrone IRP \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **\_opération de création d’IRP \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**\_opération de lecture IRP \_**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **\_opération d’écriture de l’IRP \_**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **\_opération de fermeture de l’IRP \_**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **fin de l' \_ \_ e/s DIFFÉRÉe IRP \_**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
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

 

 




