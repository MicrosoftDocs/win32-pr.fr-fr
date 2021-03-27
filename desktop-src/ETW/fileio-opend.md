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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758428"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="49bdb-104">FileIo ( \_ classe ouverte)</span><span class="sxs-lookup"><span data-stu-id="49bdb-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="49bdb-105">Cette classe est la classe de type d’événement pour les événements de fin d’opération de fichier.</span><span class="sxs-lookup"><span data-stu-id="49bdb-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="49bdb-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="49bdb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="49bdb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49bdb-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="49bdb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="49bdb-108">Members</span></span>

<span data-ttu-id="49bdb-109">La classe **FileIo \_ Opened** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49bdb-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="49bdb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49bdb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49bdb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49bdb-111">Properties</span></span>

<span data-ttu-id="49bdb-112">La classe **FileIo \_ Opened** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="49bdb-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49bdb-113">**Argument**</span><span class="sxs-lookup"><span data-stu-id="49bdb-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49bdb-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49bdb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49bdb-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49bdb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49bdb-116">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="49bdb-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="49bdb-117">Informations supplémentaires retournées par le système de fichiers pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="49bdb-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="49bdb-118">Par exemple, pour une demande de lecture, nombre réel d’octets qui ont été lus.</span><span class="sxs-lookup"><span data-stu-id="49bdb-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="49bdb-119">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="49bdb-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49bdb-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49bdb-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49bdb-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49bdb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49bdb-122">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="49bdb-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="49bdb-123">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="49bdb-123">IO request packet.</span></span> <span data-ttu-id="49bdb-124">Cette propriété identifie l’activité d’e/s qui se termine.</span><span class="sxs-lookup"><span data-stu-id="49bdb-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="49bdb-125">**NtStatus**</span><span class="sxs-lookup"><span data-stu-id="49bdb-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49bdb-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49bdb-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49bdb-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49bdb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49bdb-128">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="49bdb-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="49bdb-129">Valeur de retour de l’opération.</span><span class="sxs-lookup"><span data-stu-id="49bdb-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49bdb-130">Notes</span><span class="sxs-lookup"><span data-stu-id="49bdb-130">Remarks</span></span>

<span data-ttu-id="49bdb-131">Les événements [**FileIo**](fileio.md) sont journalisés au début de l’opération.</span><span class="sxs-lookup"><span data-stu-id="49bdb-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="49bdb-132">Les événements ouverts peuvent être activés séparément pour indiquer la fin de ces opérations.</span><span class="sxs-lookup"><span data-stu-id="49bdb-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="49bdb-133">La IRP peut être utilisée pour mettre en corrélation les événements de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="49bdb-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="49bdb-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="49bdb-134">Requirements</span></span>



| <span data-ttu-id="49bdb-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49bdb-135">Requirement</span></span> | <span data-ttu-id="49bdb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="49bdb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49bdb-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49bdb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="49bdb-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49bdb-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49bdb-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49bdb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="49bdb-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49bdb-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49bdb-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49bdb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49bdb-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="49bdb-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




