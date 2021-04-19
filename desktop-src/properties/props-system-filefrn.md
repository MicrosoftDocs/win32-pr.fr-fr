---
description: ID unique du fichier, également appelé numéro de référence du fichier.
ms.assetid: 65189671-1b55-4933-9dee-a120b38caa98
title: System. FileFRN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aa536e0cdda3f42fd9e03315156716ef499c5f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536684"
---
# <a name="systemfilefrn"></a><span data-ttu-id="14e65-103">System. FileFRN</span><span class="sxs-lookup"><span data-stu-id="14e65-103">System.FileFRN</span></span>

<span data-ttu-id="14e65-104">ID unique du fichier, également appelé numéro de référence du fichier.</span><span class="sxs-lookup"><span data-stu-id="14e65-104">The unique file ID, also known as the File Reference Number.</span></span> <span data-ttu-id="14e65-105">Pour un fichier donné, il s’agit de la même valeur que le membre **fileid** de l’ID de fichier de la structure d' [**\_ \_ \_ \_ informations de répertoire**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) , qui est obtenue par un appel à [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span><span class="sxs-lookup"><span data-stu-id="14e65-105">For a given file, this is the same value as the **FileId** member of the [**FILE\_ID\_BOTH\_DIR\_INFO**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) structure, which is obtained by a call to [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="14e65-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14e65-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileFRN
   shellPKey = PKEY_FileFRN
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 21
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="14e65-107">Notes</span><span class="sxs-lookup"><span data-stu-id="14e65-107">Remarks</span></span>

<span data-ttu-id="14e65-108">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="14e65-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14e65-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14e65-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e65-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="14e65-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="14e65-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="14e65-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="14e65-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="14e65-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="14e65-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="14e65-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="14e65-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="14e65-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="14e65-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="14e65-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="14e65-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="14e65-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="14e65-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="14e65-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="14e65-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="14e65-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="14e65-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="14e65-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="14e65-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="14e65-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="14e65-121">editControl</span><span class="sxs-lookup"><span data-stu-id="14e65-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="14e65-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="14e65-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="14e65-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="14e65-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
