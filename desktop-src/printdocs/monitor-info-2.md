---
description: La \_ structure information \_ d’analyse 2 identifie une analyse.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Structure MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759657"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="4e5fa-103">Structure du moniteur \_ informations \_ 2</span><span class="sxs-lookup"><span data-stu-id="4e5fa-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="4e5fa-104">La **structure \_ information \_ d’analyse 2** identifie une analyse.</span><span class="sxs-lookup"><span data-stu-id="4e5fa-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e5fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e5fa-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="4e5fa-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4e5fa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e5fa-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="4e5fa-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="4e5fa-108">Pointeur vers une chaîne se terminant par un caractère null qui est le nom de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="4e5fa-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4e5fa-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="4e5fa-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="4e5fa-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le moniteur a été écrit (par exemple, Windows NT x86, Windows IA64, Windows x64).</span><span class="sxs-lookup"><span data-stu-id="4e5fa-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="4e5fa-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="4e5fa-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="4e5fa-112">Pointeur vers une chaîne se terminant par un caractère null qui est le nom de la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="4e5fa-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e5fa-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e5fa-113">Requirements</span></span>



| <span data-ttu-id="4e5fa-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e5fa-114">Requirement</span></span> | <span data-ttu-id="4e5fa-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e5fa-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e5fa-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e5fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4e5fa-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e5fa-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e5fa-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e5fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4e5fa-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e5fa-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e5fa-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e5fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e5fa-121"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e5fa-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4e5fa-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4e5fa-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4e5fa-123">**\_ Analyser les \_ informations \_ 2S** (Unicode) et **\_ \_ informations sur le moniteur \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4e5fa-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4e5fa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e5fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e5fa-125">Impression</span><span class="sxs-lookup"><span data-stu-id="4e5fa-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4e5fa-126">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="4e5fa-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4e5fa-127">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="4e5fa-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="4e5fa-128">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="4e5fa-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="4e5fa-129">**\_Informations sur le moniteur \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4e5fa-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




