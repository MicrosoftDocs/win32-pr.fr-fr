---
description: Cette classe est la classe de type d’événement pour les événements d’e/s de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: Classe FileIo_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: a25c96a8a3db11f577e7780d9f12448a8a0039dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972131"
---
# <a name="fileio_name-class"></a><span data-ttu-id="cba53-104">\_Classe de nom FileIo</span><span class="sxs-lookup"><span data-stu-id="cba53-104">FileIo\_Name class</span></span>

<span data-ttu-id="cba53-105">Cette classe est la classe de type d’événement pour les événements d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="cba53-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="cba53-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="cba53-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba53-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cba53-107">Syntax</span></span>

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="cba53-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cba53-108">Members</span></span>

<span data-ttu-id="cba53-109">La classe de **\_ nom FileIo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cba53-109">The **FileIo\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="cba53-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cba53-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cba53-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cba53-111">Properties</span></span>

<span data-ttu-id="cba53-112">La classe de **\_ nom FileIo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cba53-112">The **FileIo\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cba53-113">FileName</span><span class="sxs-lookup"><span data-stu-id="cba53-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba53-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cba53-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cba53-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cba53-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cba53-116">Qualificateurs : WmiDataId (2), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="cba53-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="cba53-117">Chemin d’accès complet au fichier, à l’exclusion de la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="cba53-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="cba53-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="cba53-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba53-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cba53-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cba53-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cba53-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cba53-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="cba53-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cba53-122">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement [**\_ TypeGroup1 e**](diskio-typegroup1.md) pour déterminer le type d’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="cba53-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cba53-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cba53-123">Remarks</span></span>

<span data-ttu-id="cba53-124">**Windows Server 2003 :** Pour récupérer la lettre de lecteur pour le chemin d’accès au nom de fichier, utilisez la valeur de propriété **FileObject** pour effectuer un mappage à l’événement [ \_ TypeGroup1 e](diskio-typegroup1.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="cba53-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="cba53-125">À partir de l' \_ événement e TypeGroup1, utilisez les valeurs de propriété **DiskNumber** et **ByteOffset** pour mapper à l’événement SystemConfig [ \_ LogDisk](systemconfig-logdisk.md) correspondant (**ByteOffset** est mappé à **StartOffset**).</span><span class="sxs-lookup"><span data-stu-id="cba53-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="cba53-126">La propriété **DriveLetterString** contient la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="cba53-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba53-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cba53-127">Requirements</span></span>



| <span data-ttu-id="cba53-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cba53-128">Requirement</span></span> | <span data-ttu-id="cba53-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cba53-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cba53-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba53-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cba53-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba53-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cba53-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba53-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cba53-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba53-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cba53-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba53-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba53-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="cba53-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




