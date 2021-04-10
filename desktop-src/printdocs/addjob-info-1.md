---
description: La \_ structure ADDJOB info \_ 1 identifie un travail d’impression ainsi que le répertoire et le fichier dans lequel une application peut stocker ce travail.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Structure ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210476"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="bb0e8-103">ADDJOB \_ information \_ 1 (structure)</span><span class="sxs-lookup"><span data-stu-id="bb0e8-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="bb0e8-104">La structure **ADDJOB \_ info \_ 1** identifie un travail d’impression ainsi que le répertoire et le fichier dans lequel une application peut stocker ce travail.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb0e8-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="bb0e8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="bb0e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb0e8-107">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="bb0e8-108">Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès et le nom de fichier que l’application peut utiliser pour stocker le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="bb0e8-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="bb0e8-110">Handle du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb0e8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb0e8-111">Requirements</span></span>



| <span data-ttu-id="bb0e8-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb0e8-112">Requirement</span></span> | <span data-ttu-id="bb0e8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0e8-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0e8-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb0e8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bb0e8-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb0e8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb0e8-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb0e8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bb0e8-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb0e8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb0e8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb0e8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb0e8-119"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb0e8-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bb0e8-120">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="bb0e8-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb0e8-121">**\_ ADDJOB \_ info \_ 1s** (Unicode) et **\_ ADDJOB \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb0e8-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="bb0e8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb0e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0e8-123">Impression</span><span class="sxs-lookup"><span data-stu-id="bb0e8-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bb0e8-124">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="bb0e8-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bb0e8-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




