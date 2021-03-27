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
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971946"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="5e034-104">E \_ TypeGroup3, classe</span><span class="sxs-lookup"><span data-stu-id="5e034-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="5e034-105">Cette classe est la classe de type d’événement pour les événements de vidage d’e/s de disque.</span><span class="sxs-lookup"><span data-stu-id="5e034-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="5e034-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="5e034-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e034-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e034-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5e034-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5e034-108">Members</span></span>

<span data-ttu-id="5e034-109">La classe **e \_ TypeGroup3** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5e034-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="5e034-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e034-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e034-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e034-111">Properties</span></span>

<span data-ttu-id="5e034-112">La classe **e \_ TypeGroup3** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e034-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e034-113">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="5e034-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e034-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e034-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-116">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="5e034-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5e034-117">Numéro qui identifie le disque physique.</span><span class="sxs-lookup"><span data-stu-id="5e034-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-118">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="5e034-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-119">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e034-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e034-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-121">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="5e034-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="5e034-122">Nombre de cycles de l’UC à partir du début de l’opération jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5e034-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-123">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="5e034-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e034-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e034-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-126">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**pointeur**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5e034-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5e034-127">Paquet de requête d’e/s.</span><span class="sxs-lookup"><span data-stu-id="5e034-127">I/O request packet.</span></span> <span data-ttu-id="5e034-128">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="5e034-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-129">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="5e034-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e034-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e034-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-132">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="5e034-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="5e034-133">Peut contenir un ou plusieurs des indicateurs de paquets de requêtes d’e/s suivants (définis dans Ntddk. h, qui est un fichier d’en-tête DDK) :</span><span class="sxs-lookup"><span data-stu-id="5e034-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="5e034-134">**IRP \_ NOcache**</span><span class="sxs-lookup"><span data-stu-id="5e034-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="5e034-135">**\_ \_ e/s de pagination IRP**</span><span class="sxs-lookup"><span data-stu-id="5e034-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="5e034-136">**\_achèvement du montage IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="5e034-137">**API de l’IRP \_ synchrone \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="5e034-138">**\_IRP associée de la IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="5e034-139">**\_e/s mises en mémoire tampon IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="5e034-140">**\_mémoire tampon d’IRP DEALLOCATE \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="5e034-141">**\_opération d’entrée IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="5e034-142">**\_ \_ e/s de pagination synchrone IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="5e034-143">**\_opération de création d’IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="5e034-144">**\_opération de lecture IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="5e034-145">**\_opération d’écriture de l’IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="5e034-146">**\_opération de fermeture de l’IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="5e034-147">**fin de l' \_ \_ e/s DIFFÉRÉe IRP \_**</span><span class="sxs-lookup"><span data-stu-id="5e034-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e034-148">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="5e034-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e034-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e034-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-151">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="5e034-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="5e034-152">Identificateur du thread émetteur.</span><span class="sxs-lookup"><span data-stu-id="5e034-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="5e034-153">**Windows server 2008 R2, Windows server 2008, Windows 7 et Windows Vista :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e034-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e034-154">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e034-154">Requirements</span></span>



| <span data-ttu-id="5e034-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e034-155">Requirement</span></span> | <span data-ttu-id="5e034-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e034-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e034-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e034-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5e034-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e034-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e034-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e034-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5e034-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e034-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e034-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e034-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e034-162">**E**</span><span class="sxs-lookup"><span data-stu-id="5e034-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




