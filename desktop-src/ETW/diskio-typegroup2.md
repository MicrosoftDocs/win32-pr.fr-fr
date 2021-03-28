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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525263"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="bfa63-104">E \_ TypeGroup2, classe</span><span class="sxs-lookup"><span data-stu-id="bfa63-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="bfa63-105">Cette classe est la classe de type d’événement qui marque le début des événements de lecture, d’écriture et de vidage des e/s disque.</span><span class="sxs-lookup"><span data-stu-id="bfa63-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="bfa63-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="bfa63-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa63-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfa63-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="bfa63-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bfa63-108">Members</span></span>

<span data-ttu-id="bfa63-109">La classe **e \_ TypeGroup2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bfa63-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="bfa63-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfa63-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfa63-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfa63-111">Properties</span></span>

<span data-ttu-id="bfa63-112">La classe **e \_ TypeGroup2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="bfa63-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfa63-113">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="bfa63-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa63-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bfa63-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfa63-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bfa63-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa63-116">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**pointeur**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bfa63-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bfa63-117">Paquet de requête d’e/s.</span><span class="sxs-lookup"><span data-stu-id="bfa63-117">I/O request packet.</span></span> <span data-ttu-id="bfa63-118">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="bfa63-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="bfa63-119">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="bfa63-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa63-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bfa63-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfa63-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bfa63-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa63-122">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="bfa63-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="bfa63-123">Identificateur du thread émetteur.</span><span class="sxs-lookup"><span data-stu-id="bfa63-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="bfa63-124">**Windows server 2008 R2, Windows server 2008, Windows 7 et Windows Vista :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bfa63-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfa63-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bfa63-125">Requirements</span></span>



| <span data-ttu-id="bfa63-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfa63-126">Requirement</span></span> | <span data-ttu-id="bfa63-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfa63-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bfa63-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa63-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa63-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa63-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bfa63-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa63-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa63-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa63-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bfa63-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfa63-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa63-133">**E**</span><span class="sxs-lookup"><span data-stu-id="bfa63-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




