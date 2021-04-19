---
description: La \_ structure information \_ d’analyse 1 identifie un moniteur installé.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Structure MONITOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527879"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="d48c5-103">Structure d’information d’analyse \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="d48c5-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="d48c5-104">La **structure \_ information \_ d’analyse 1** identifie un moniteur installé.</span><span class="sxs-lookup"><span data-stu-id="d48c5-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d48c5-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="d48c5-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d48c5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d48c5-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="d48c5-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="d48c5-108">Pointeur vers une chaîne se terminant par un caractère null qui identifie un moniteur installé.</span><span class="sxs-lookup"><span data-stu-id="d48c5-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d48c5-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d48c5-109">Requirements</span></span>



| <span data-ttu-id="d48c5-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d48c5-110">Requirement</span></span> | <span data-ttu-id="d48c5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="d48c5-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d48c5-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48c5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d48c5-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d48c5-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d48c5-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48c5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d48c5-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d48c5-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d48c5-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d48c5-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d48c5-117"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d48c5-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d48c5-118">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d48c5-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d48c5-119">**\_ Analyser les \_ informations \_ 1s** (Unicode) et **\_ \_ informations sur le moniteur \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d48c5-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="d48c5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d48c5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48c5-121">Impression</span><span class="sxs-lookup"><span data-stu-id="d48c5-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d48c5-122">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d48c5-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="d48c5-123">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="d48c5-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="d48c5-124">**\_Informations sur le moniteur \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d48c5-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




