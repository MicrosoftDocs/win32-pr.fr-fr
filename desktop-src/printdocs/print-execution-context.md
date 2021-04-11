---
description: Représente le contexte d’exécution lorsque GetPrintExecutionData est appelé.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Énumération PRINT_EXECUTION_CONTEXT (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202806"
---
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="d0dab-103">\_Énumération du contexte d’exécution d’impression \_</span><span class="sxs-lookup"><span data-stu-id="d0dab-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="d0dab-104">Représente le contexte d’exécution lorsque [**GetPrintExecutionData**](getprintexecutiondata.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="d0dab-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0dab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0dab-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="d0dab-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d0dab-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d0dab-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**Imprimer \_ le \_ contexte d’exécution \_ application**</span><span class="sxs-lookup"><span data-stu-id="d0dab-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="d0dab-108">L’appelant est en cours d’exécution dans une application.</span><span class="sxs-lookup"><span data-stu-id="d0dab-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="d0dab-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ service spouleur du contexte d’exécution d’impression \_**</span><span class="sxs-lookup"><span data-stu-id="d0dab-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="d0dab-110">L’appelant est en cours d’exécution dans le service de spouleur (spoolsv.exe).</span><span class="sxs-lookup"><span data-stu-id="d0dab-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="d0dab-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ hôte d’isolation du spouleur du contexte \_ d’exécution d' \_ impression**</span><span class="sxs-lookup"><span data-stu-id="d0dab-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="d0dab-112">L’appelant est en cours d’exécution dans l’hôte d’isolation d’impression (PrintIsolationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="d0dab-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="d0dab-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**Imprimer \_ le \_ \_ pipeline du filtre du contexte d’exécution \_**</span><span class="sxs-lookup"><span data-stu-id="d0dab-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="d0dab-114">L’appelant est en cours d’exécution dans le pipeline de filtre d’impression (printfilterpipelinesvc.exe)</span><span class="sxs-lookup"><span data-stu-id="d0dab-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="d0dab-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Contexte d’exécution d’impression \_ \_ \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="d0dab-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="d0dab-116">L’appelant est en cours d’exécution dans splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="d0dab-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0dab-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0dab-117">Requirements</span></span>



| <span data-ttu-id="d0dab-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0dab-118">Requirement</span></span> | <span data-ttu-id="d0dab-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0dab-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0dab-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0dab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0dab-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0dab-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="d0dab-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0dab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0dab-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0dab-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d0dab-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0dab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0dab-125"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0dab-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0dab-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0dab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0dab-127">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="d0dab-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="d0dab-128">**Imprimer \_ les \_ données d’exécution**</span><span class="sxs-lookup"><span data-stu-id="d0dab-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




