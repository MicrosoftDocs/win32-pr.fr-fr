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
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="52f6d-104">E \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="52f6d-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="52f6d-105">Cette classe est la classe de type d’événement pour les événements d’e/s de disque.</span><span class="sxs-lookup"><span data-stu-id="52f6d-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="52f6d-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="52f6d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f6d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52f6d-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="52f6d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="52f6d-108">Members</span></span>

<span data-ttu-id="52f6d-109">La classe **e \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52f6d-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="52f6d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52f6d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52f6d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52f6d-111">Properties</span></span>

<span data-ttu-id="52f6d-112">La classe **e \_ TypeGroup1** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="52f6d-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52f6d-113">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="52f6d-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-114">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="52f6d-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-116">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="52f6d-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-117">Offset d’octet à partir du début du disque physique.</span><span class="sxs-lookup"><span data-stu-id="52f6d-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-118">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="52f6d-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-121">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="52f6d-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-122">Numéro qui identifie le disque physique.</span><span class="sxs-lookup"><span data-stu-id="52f6d-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="52f6d-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-126">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**pointeur**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="52f6d-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-127">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement de [**\_ nom FileIo**](fileio-name.md) pour déterminer le fichier impliqué dans l’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="52f6d-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-128">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="52f6d-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-129">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52f6d-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-131">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span><span class="sxs-lookup"><span data-stu-id="52f6d-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-132">Délai entre l’initiation et l’achèvement des e/s, tel qu’il est mesuré par le gestionnaire de partition (dans les unités de graduation [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).</span><span class="sxs-lookup"><span data-stu-id="52f6d-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="52f6d-133">**Windows Server 2003 :** Cette propriété a une valeur [**WmiDataId**](event-tracing-mof-qualifiers.md) de 7.</span><span class="sxs-lookup"><span data-stu-id="52f6d-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="52f6d-134">**Windows 2000 Server et windows 2000 professionnel :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52f6d-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-135">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="52f6d-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-136">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-138">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**pointeur**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="52f6d-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-139">Le paquet de requête d’e/s, qui identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="52f6d-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="52f6d-140">**Windows server 2003, windows 2000 Server et windows 2000 professionnel :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52f6d-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-141">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="52f6d-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-144">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="52f6d-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-145">Peut contenir un ou plusieurs des indicateurs de paquets de requêtes d’e/s suivants (définis dans Ntddk. h, qui est un fichier d’en-tête DDK) :</span><span class="sxs-lookup"><span data-stu-id="52f6d-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="52f6d-146">**IRP \_ NOcache**</span><span class="sxs-lookup"><span data-stu-id="52f6d-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="52f6d-147">**\_ \_ e/s de pagination IRP**</span><span class="sxs-lookup"><span data-stu-id="52f6d-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="52f6d-148">**\_achèvement du montage IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="52f6d-149">**API de l’IRP \_ synchrone \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="52f6d-150">**\_IRP associée de la IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="52f6d-151">**\_e/s mises en mémoire tampon IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="52f6d-152">**\_mémoire tampon d’IRP DEALLOCATE \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="52f6d-153">**\_opération d’entrée IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="52f6d-154">**\_ \_ e/s de pagination synchrone IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="52f6d-155">**\_opération de création d’IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="52f6d-156">**\_opération de lecture IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="52f6d-157">**\_opération d’écriture de l’IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="52f6d-158">**\_opération de fermeture de l’IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="52f6d-159">**fin de l' \_ \_ e/s DIFFÉRÉe IRP \_**</span><span class="sxs-lookup"><span data-stu-id="52f6d-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52f6d-160">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="52f6d-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-163">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span><span class="sxs-lookup"><span data-stu-id="52f6d-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-164">Identificateur du thread émetteur.</span><span class="sxs-lookup"><span data-stu-id="52f6d-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="52f6d-165">**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 avec SP1, Windows server 2003, windows 2000 Server et windows 2000 professionnel :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52f6d-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-166">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="52f6d-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-169">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="52f6d-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-170">Réservé.</span><span class="sxs-lookup"><span data-stu-id="52f6d-170">Reserved.</span></span>

<span data-ttu-id="52f6d-171">**Windows server 2008 R2, Windows server 2008 et Windows 7 :** Le nom de la propriété est **QueueDepth**, qui contient le nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="52f6d-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="52f6d-172">Notez que cette valeur peut provoquer un dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="52f6d-172">Note that this value can overflow.</span></span>

<span data-ttu-id="52f6d-173">**Windows Vista, Windows server 2003 avec SP1, Windows server 2003, windows 2000 Server et windows 2000 professionnel :** Le nom de la propriété est **ResponseTime**, qui contient le nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="52f6d-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="52f6d-174">Notez que cette valeur peut provoquer un dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="52f6d-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="52f6d-175">**Transférer**</span><span class="sxs-lookup"><span data-stu-id="52f6d-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f6d-176">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52f6d-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52f6d-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f6d-178">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="52f6d-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="52f6d-179">Taille des données lues ou écrites à partir du disque, en octets.</span><span class="sxs-lookup"><span data-stu-id="52f6d-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52f6d-180">Notes</span><span class="sxs-lookup"><span data-stu-id="52f6d-180">Remarks</span></span>

<span data-ttu-id="52f6d-181">Windows Server 2003 utilise la définition suivante pour la classe de type d’événement **e \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="52f6d-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="52f6d-182">La propriété **ResponseTime** contient le nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="52f6d-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="52f6d-183">Notez que cette valeur peut provoquer un dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="52f6d-183">Note that this value can overflow.</span></span>

<span data-ttu-id="52f6d-184">La propriété **HighResResponseTime** n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52f6d-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="52f6d-185">Windows Server 2003 avec SP1 et Windows Vista utilise la définition suivante pour la classe de type d’événement **e \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="52f6d-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="52f6d-186">La propriété **IRP** est le paquet de requête d’e/s.</span><span class="sxs-lookup"><span data-stu-id="52f6d-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="52f6d-187">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="52f6d-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="52f6d-188">Vous pouvez utiliser cette propriété avec les événements [**e \_ TypeGroup2**](diskio-typegroup2.md) pour corréler le temps de réponse.</span><span class="sxs-lookup"><span data-stu-id="52f6d-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="52f6d-189">La propriété **HighResResponseTime** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52f6d-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="52f6d-190">La propriété contient le temps entre le début et l’achèvement des e/s, tel qu’il est mesuré par PartitionManager (dans les unités KeQueryPerformanceCounter).</span><span class="sxs-lookup"><span data-stu-id="52f6d-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="52f6d-191">Utilisez cette propriété à la place de la propriété **ResponseTime** pour déterminer le temps de réponse des e/s disque.</span><span class="sxs-lookup"><span data-stu-id="52f6d-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f6d-192">Spécifications</span><span class="sxs-lookup"><span data-stu-id="52f6d-192">Requirements</span></span>



| <span data-ttu-id="52f6d-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52f6d-193">Requirement</span></span> | <span data-ttu-id="52f6d-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="52f6d-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="52f6d-195">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52f6d-195">Minimum supported client</span></span><br/> | <span data-ttu-id="52f6d-196">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52f6d-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="52f6d-197">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52f6d-197">Minimum supported server</span></span><br/> | <span data-ttu-id="52f6d-198">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52f6d-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="52f6d-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52f6d-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f6d-200">**E**</span><span class="sxs-lookup"><span data-stu-id="52f6d-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 
