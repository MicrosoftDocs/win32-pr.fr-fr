---
description: Cette classe est la classe de type d’événement pour l’événement d’informations de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Classe FileIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973558"
---
# <a name="fileio_info-class"></a><span data-ttu-id="3991a-104">FileIo \_ info (classe)</span><span class="sxs-lookup"><span data-stu-id="3991a-104">FileIo\_Info class</span></span>

<span data-ttu-id="3991a-105">Cette classe est la classe de type d’événement pour l’événement d’informations de fichier.</span><span class="sxs-lookup"><span data-stu-id="3991a-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="3991a-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="3991a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3991a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3991a-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="3991a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3991a-108">Members</span></span>

<span data-ttu-id="3991a-109">La classe d' **\_ informations FileIo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3991a-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="3991a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3991a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3991a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3991a-111">Properties</span></span>

<span data-ttu-id="3991a-112">La classe d' **\_ informations FileIo** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3991a-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3991a-113">**Argument**</span><span class="sxs-lookup"><span data-stu-id="3991a-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3991a-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3991a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3991a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3991a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3991a-116">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="3991a-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3991a-117">Pour les demandes FileDispositionInformation, ce champ contient la disposition demandée.</span><span class="sxs-lookup"><span data-stu-id="3991a-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="3991a-118">Pour les demandes FileEndOfFileInformation et FileAllocationInformation, ce champ contient la taille de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3991a-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-119">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="3991a-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3991a-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3991a-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3991a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3991a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3991a-122">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="3991a-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3991a-123">Pour déterminer le nom de fichier, faites correspondre la valeur de cette propriété à la propriété **FileObject** d’un événement de [**\_ nom FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="3991a-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-124">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="3991a-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3991a-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3991a-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3991a-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3991a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3991a-127">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="3991a-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3991a-128">Identificateur qui peut être utilisé pour mettre en corrélation des opérations avec la même instance d’objet de fichier ouverte entre les événements de création et de fermeture de fichier.</span><span class="sxs-lookup"><span data-stu-id="3991a-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-129">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="3991a-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3991a-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3991a-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3991a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3991a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3991a-132">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="3991a-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="3991a-133">Classe d’informations de fichier demandée.</span><span class="sxs-lookup"><span data-stu-id="3991a-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-134">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="3991a-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3991a-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3991a-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3991a-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3991a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3991a-137">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="3991a-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3991a-138">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="3991a-138">IO request packet.</span></span> <span data-ttu-id="3991a-139">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="3991a-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-140">**TTID**</span><span class="sxs-lookup"><span data-stu-id="3991a-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3991a-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3991a-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3991a-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3991a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3991a-143">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="3991a-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3991a-144">Identificateur du thread qui effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="3991a-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3991a-145">Notes</span><span class="sxs-lookup"><span data-stu-id="3991a-145">Remarks</span></span>

<span data-ttu-id="3991a-146">Définir des informations et des événements d’informations de requête indique que les attributs de fichier ont été définis ou interrogés.</span><span class="sxs-lookup"><span data-stu-id="3991a-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="3991a-147">Un événement de contrôle de système de fichiers (FSControl) est enregistré lors de l’émission d’une commande FSCTL.</span><span class="sxs-lookup"><span data-stu-id="3991a-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="3991a-148">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3991a-148">Requirements</span></span>



| <span data-ttu-id="3991a-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3991a-149">Requirement</span></span> | <span data-ttu-id="3991a-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="3991a-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3991a-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3991a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3991a-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3991a-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3991a-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3991a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3991a-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3991a-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3991a-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3991a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3991a-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="3991a-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




