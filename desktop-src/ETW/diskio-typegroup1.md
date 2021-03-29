---
description: Cette classe est la classe de type d’événement pour les événements d’e/s de disque. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: Classe DiskIo_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526866"
---
# <a name="diskio_typegroup1-class"></a>E \_ TypeGroup1, classe

Cette classe est la classe de type d’événement pour les événements d’e/s de disque.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Membres

La classe **e \_ TypeGroup1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **e \_ TypeGroup1** possède les propriétés suivantes.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Type de données : **sint64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Offset d’octet à partir du début du disque physique.

</dd> <dt>

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

**FileObject**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**pointeur**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement de [**\_ nom FileIo**](fileio-name.md) pour déterminer le fichier impliqué dans l’opération d’e/s.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Délai entre l’initiation et l’achèvement des e/s, tel qu’il est mesuré par le gestionnaire de partition (dans les unités de graduation [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).

**Windows Server 2003 :** Cette propriété a une valeur [**WmiDataId**](event-tracing-mof-qualifiers.md) de 7.

**Windows 2000 Server et windows 2000 professionnel :** Cette propriété n’est pas prise en charge.

</dd> <dt>

**Paquets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**pointeur**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Le paquet de requête d’e/s, qui identifie l’activité d’e/s.

**Windows server 2003, windows 2000 Server et windows 2000 professionnel :** Cette propriété n’est pas prise en charge.

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

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Identificateur du thread émetteur.

**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 avec SP1, Windows server 2003, windows 2000 Server et windows 2000 professionnel :** Cette propriété n’est pas prise en charge.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Réservé.

**Windows server 2008 R2, Windows server 2008 et Windows 7 :** Le nom de la propriété est **QueueDepth**, qui contient le nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération. Notez que cette valeur peut provoquer un dépassement de capacité.

**Windows Vista, Windows server 2003 avec SP1, Windows server 2003, windows 2000 Server et windows 2000 professionnel :** Le nom de la propriété est **ResponseTime**, qui contient le nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération. Notez que cette valeur peut provoquer un dépassement de capacité.

</dd> <dt>

**Transférer**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Taille des données lues ou écrites à partir du disque, en octets.

</dd> </dl>

## <a name="remarks"></a>Notes

Windows Server 2003 utilise la définition suivante pour la classe de type d’événement **e \_ TypeGroup1** .

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

La propriété **ResponseTime** contient le nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération. Notez que cette valeur peut provoquer un dépassement de capacité.

La propriété **HighResResponseTime** n’est pas prise en charge.

Windows Server 2003 avec SP1 et Windows Vista utilise la définition suivante pour la classe de type d’événement **e \_ TypeGroup1** .

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

La propriété **IRP** est le paquet de requête d’e/s. Cette propriété identifie l’activité d’e/s. Vous pouvez utiliser cette propriété avec les événements [**e \_ TypeGroup2**](diskio-typegroup2.md) pour corréler le temps de réponse.

La propriété **HighResResponseTime** est prise en charge. La propriété contient le temps entre le début et l’achèvement des e/s, tel qu’il est mesuré par PartitionManager (dans les unités KeQueryPerformanceCounter). Utilisez cette propriété à la place de la propriété **ResponseTime** pour déterminer le temps de réponse des e/s disque.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**E**](diskio.md)
</dt> </dl>

 

 
