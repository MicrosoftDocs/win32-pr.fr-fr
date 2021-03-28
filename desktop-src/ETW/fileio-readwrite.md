---
description: Cette classe est la classe de type d’événement pour les événements de lecture et d’écriture de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: Classe FileIo_ReadWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973555"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="9d6ed-104">FileIo \_ ReadWrite, classe</span><span class="sxs-lookup"><span data-stu-id="9d6ed-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="9d6ed-105">Cette classe est la classe de type d’événement pour les événements de lecture et d’écriture de fichier.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="9d6ed-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6ed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d6ed-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="9d6ed-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9d6ed-108">Members</span></span>

<span data-ttu-id="9d6ed-109">La classe **FileIo \_ ReadWrite** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9d6ed-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="9d6ed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d6ed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d6ed-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d6ed-111">Properties</span></span>

<span data-ttu-id="9d6ed-112">La classe **FileIo \_ ReadWrite** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d6ed-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-116">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="9d6ed-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-117">Pour déterminer le nom de fichier, faites correspondre la valeur de cette propriété à la propriété **FileObject** d’un événement de [**\_ nom FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="9d6ed-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="9d6ed-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-121">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="9d6ed-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-122">Identificateur qui peut être utilisé pour mettre en corrélation des opérations avec la même instance d’objet de fichier ouverte entre les événements de création et de fermeture de fichier.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="9d6ed-123">**IoFlags**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-126">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="9d6ed-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-127">Indicateurs de paquets de demande d’e/s spécifiés pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9d6ed-128">**IoSize**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-131">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="9d6ed-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-132">Nombre d’octets demandés.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="9d6ed-133">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-136">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="9d6ed-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-137">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-137">IO request packet.</span></span> <span data-ttu-id="9d6ed-138">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="9d6ed-139">**Offset**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-140">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-142">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9d6ed-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-143">Début du décalage de fichier pour l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="9d6ed-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d6ed-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d6ed-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d6ed-147">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="9d6ed-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9d6ed-148">Identificateur du thread qui effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="9d6ed-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d6ed-149">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d6ed-149">Requirements</span></span>



| <span data-ttu-id="9d6ed-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d6ed-150">Requirement</span></span> | <span data-ttu-id="9d6ed-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d6ed-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d6ed-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6ed-152">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6ed-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d6ed-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d6ed-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6ed-154">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6ed-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d6ed-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d6ed-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6ed-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6ed-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="9d6ed-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




