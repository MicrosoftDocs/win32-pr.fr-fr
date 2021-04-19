---
description: La \_ structure PRINTPROCESSOR info \_ 1 spécifie le nom d’un processeur d’impression installé.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Structure PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545016"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="93fa0-103">PRINTPROCESSOR \_ information \_ 1 (structure)</span><span class="sxs-lookup"><span data-stu-id="93fa0-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="93fa0-104">La structure **PRINTPROCESSOR \_ info \_ 1** spécifie le nom d’un processeur d’impression installé.</span><span class="sxs-lookup"><span data-stu-id="93fa0-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="93fa0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93fa0-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="93fa0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="93fa0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="93fa0-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="93fa0-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="93fa0-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un processeur d’impression installé.</span><span class="sxs-lookup"><span data-stu-id="93fa0-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93fa0-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93fa0-109">Requirements</span></span>



| <span data-ttu-id="93fa0-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93fa0-110">Requirement</span></span> | <span data-ttu-id="93fa0-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="93fa0-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93fa0-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93fa0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="93fa0-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93fa0-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93fa0-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93fa0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="93fa0-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93fa0-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93fa0-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="93fa0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="93fa0-117"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93fa0-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="93fa0-118">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="93fa0-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="93fa0-119">**\_ PRINTPROCESSOR \_ info \_ 1s** (Unicode) et **\_ PRINTPROCESSOR \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="93fa0-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="93fa0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93fa0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93fa0-121">Impression</span><span class="sxs-lookup"><span data-stu-id="93fa0-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="93fa0-122">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="93fa0-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="93fa0-123">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="93fa0-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




