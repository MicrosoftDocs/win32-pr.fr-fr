---
description: Cette classe est la classe de type d’événement pour l’événement de création de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: Classe FileIo_Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972203"
---
# <a name="fileio_create-class"></a><span data-ttu-id="f9539-104">FileIo \_ créer une classe</span><span class="sxs-lookup"><span data-stu-id="f9539-104">FileIo\_Create class</span></span>

<span data-ttu-id="f9539-105">Cette classe est la classe de type d’événement pour l’événement de création de fichier.</span><span class="sxs-lookup"><span data-stu-id="f9539-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="f9539-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="f9539-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9539-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9539-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="f9539-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f9539-108">Members</span></span>

<span data-ttu-id="f9539-109">La classe de **\_ création FileIo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f9539-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="f9539-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f9539-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9539-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f9539-111">Properties</span></span>

<span data-ttu-id="f9539-112">La classe de **\_ création FileIo** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f9539-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9539-113">**CreateOptions**</span><span class="sxs-lookup"><span data-stu-id="f9539-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9539-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-116">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="f9539-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f9539-117">Valeurs passées dans les paramètres *CreateOptions* et *CreateDispositions* à la fonction [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="f9539-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="f9539-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="f9539-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9539-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-121">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="f9539-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="f9539-122">Valeur transmise dans le paramètre *FileAttributes* à la fonction [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="f9539-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="f9539-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="f9539-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9539-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-126">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="f9539-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9539-127">Identificateur qui peut être utilisé pour mettre en corrélation des opérations avec la même instance d’objet de fichier ouverte entre les événements de création et de fermeture de fichier.</span><span class="sxs-lookup"><span data-stu-id="f9539-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="f9539-128">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="f9539-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9539-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-131">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="f9539-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9539-132">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="f9539-132">IO request packet.</span></span> <span data-ttu-id="f9539-133">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="f9539-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="f9539-134">**OpenPath**</span><span class="sxs-lookup"><span data-stu-id="f9539-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9539-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-137">Qualificateurs : WmiDataId (7), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="f9539-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="f9539-138">Chemin d'accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="f9539-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="f9539-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="f9539-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9539-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-142">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="f9539-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="f9539-143">Valeur transmise dans le paramètre *ShareAccess* à la fonction [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="f9539-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="f9539-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="f9539-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9539-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9539-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9539-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9539-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9539-147">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="f9539-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9539-148">Identificateur du thread qui crée le fichier.</span><span class="sxs-lookup"><span data-stu-id="f9539-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9539-149">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f9539-149">Requirements</span></span>



| <span data-ttu-id="f9539-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9539-150">Requirement</span></span> | <span data-ttu-id="f9539-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9539-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9539-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9539-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f9539-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9539-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9539-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9539-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f9539-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9539-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9539-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9539-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9539-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="f9539-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
