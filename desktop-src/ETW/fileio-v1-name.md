---
description: Cette classe est la classe de type d’événement pour les événements d’e/s de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: Classe FileIo_V1_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034805"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="a9097-104">FileIo \_ v1, \_ classe de nom</span><span class="sxs-lookup"><span data-stu-id="a9097-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="a9097-105">Cette classe est la classe de type d’événement pour les événements d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="a9097-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="a9097-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a9097-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9097-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9097-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="a9097-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a9097-108">Members</span></span>

<span data-ttu-id="a9097-109">La classe de **\_ \_ nom FileIo v1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a9097-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="a9097-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9097-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9097-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9097-111">Properties</span></span>

<span data-ttu-id="a9097-112">La classe de **\_ \_ nom FileIo v1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a9097-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9097-113">FileName</span><span class="sxs-lookup"><span data-stu-id="a9097-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9097-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9097-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9097-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9097-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9097-116">Qualificateurs : WmiDataId (2), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="a9097-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a9097-117">Chemin d’accès complet au fichier, à l’exclusion de la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="a9097-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="a9097-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="a9097-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9097-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9097-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9097-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9097-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9097-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="a9097-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a9097-122">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement [**\_ TypeGroup1 e**](diskio-typegroup1.md) pour déterminer le type d’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="a9097-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9097-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a9097-123">Remarks</span></span>

<span data-ttu-id="a9097-124">**Windows Server 2003 :** Pour récupérer la lettre de lecteur pour le chemin d’accès au nom de fichier, utilisez la valeur de propriété **FileObject** pour effectuer un mappage à l’événement [ \_ TypeGroup1 e](diskio-typegroup1.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="a9097-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="a9097-125">À partir de l' \_ événement e TypeGroup1, utilisez les valeurs de propriété **DiskNumber** et **ByteOffset** pour mapper à l’événement SystemConfig [ \_ LogDisk](systemconfig-logdisk.md) correspondant (**ByteOffset** est mappé à **StartOffset**).</span><span class="sxs-lookup"><span data-stu-id="a9097-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="a9097-126">La propriété **DriveLetterString** contient la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="a9097-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9097-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9097-127">Requirements</span></span>



| <span data-ttu-id="a9097-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9097-128">Requirement</span></span> | <span data-ttu-id="a9097-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9097-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9097-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9097-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a9097-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9097-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a9097-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9097-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a9097-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9097-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9097-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9097-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9097-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="a9097-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




