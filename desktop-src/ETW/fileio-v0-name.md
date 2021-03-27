---
description: La \_ \_ classe de nom FileIo v0 est une version antérieure de la classe de type d’événement pour les événements d’e/s de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Classe FileIo_V0_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758427"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="9278c-104">FileIo \_ v0, \_ classe de nom</span><span class="sxs-lookup"><span data-stu-id="9278c-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="9278c-105">La classe de **\_ \_ nom FileIo v0** est une version antérieure de la classe de type d’événement pour les événements d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="9278c-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="9278c-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="9278c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9278c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9278c-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="9278c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9278c-108">Members</span></span>

<span data-ttu-id="9278c-109">La classe de **\_ \_ nom FileIo v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9278c-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="9278c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9278c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9278c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9278c-111">Properties</span></span>

<span data-ttu-id="9278c-112">La classe de **\_ \_ nom FileIo v0** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9278c-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9278c-113">FileName</span><span class="sxs-lookup"><span data-stu-id="9278c-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9278c-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9278c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9278c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9278c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9278c-116">Qualificateurs : WmiDataId (2), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="9278c-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9278c-117">Chemin d’accès complet au fichier, à l’exclusion de la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="9278c-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="9278c-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="9278c-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9278c-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9278c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9278c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9278c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9278c-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="9278c-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9278c-122">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement [**\_ TypeGroup1 e**](diskio-typegroup1.md) pour déterminer le type d’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="9278c-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9278c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9278c-123">Remarks</span></span>

<span data-ttu-id="9278c-124">**Windows Server 2003 :** Pour récupérer la lettre de lecteur pour le chemin d’accès au nom de fichier, utilisez la valeur de propriété **FileObject** pour effectuer un mappage à l’événement [**\_ TypeGroup1 e**](diskio-typegroup1.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="9278c-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="9278c-125">À partir de l’événement **e \_ TypeGroup1** , utilisez les valeurs de propriété **DiskNumber** et **ByteOffset** pour mapper à l’événement SystemConfig [**\_ LogDisk**](systemconfig-logdisk.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="9278c-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="9278c-126">La propriété **DriveLetterString** contient la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="9278c-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9278c-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9278c-127">Requirements</span></span>



| <span data-ttu-id="9278c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9278c-128">Requirement</span></span> | <span data-ttu-id="9278c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9278c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9278c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9278c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9278c-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9278c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9278c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9278c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9278c-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9278c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9278c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9278c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9278c-135">**FileIo \_ v0**</span><span class="sxs-lookup"><span data-stu-id="9278c-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




