---
description: Contient le contexte d’exécution du pilote d’imprimante qui appelle GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Structure PRINT_EXECUTION_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204229"
---
# <a name="print_execution_data-structure"></a><span data-ttu-id="d450e-103">Imprimer \_ la \_ structure des données d’exécution</span><span class="sxs-lookup"><span data-stu-id="d450e-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="d450e-104">Contient le contexte d’exécution du pilote d’imprimante qui appelle [**GetPrintExecutionData**](getprintexecutiondata.md).</span><span class="sxs-lookup"><span data-stu-id="d450e-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d450e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d450e-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="d450e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d450e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d450e-107">**context**</span><span class="sxs-lookup"><span data-stu-id="d450e-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="d450e-108">Valeur [**du \_ \_ contexte d’exécution**](print-execution-context.md) de l’impression qui représente le contexte d’exécution actuel du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d450e-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="d450e-109">**clientAppPID**</span><span class="sxs-lookup"><span data-stu-id="d450e-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="d450e-110">Si la valeur de **Context** est **le \_ contexte d’exécution d’impression \_ \_ WOW64**, **clientAppPID** identifie l’application cliente au nom duquel le processus de splwow64.exe a chargé le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d450e-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="d450e-111">Si la valeur du **contexte** n’affiche pas le **\_ contexte d’exécution \_ \_ WOW64**, **clientAppPID** est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d450e-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d450e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d450e-112">Requirements</span></span>



| <span data-ttu-id="d450e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d450e-113">Requirement</span></span> | <span data-ttu-id="d450e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d450e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d450e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d450e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d450e-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d450e-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="d450e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d450e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d450e-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d450e-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d450e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d450e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d450e-120"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d450e-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d450e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d450e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d450e-122">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="d450e-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="d450e-123">**Imprimer \_ le \_ contexte d’exécution**</span><span class="sxs-lookup"><span data-stu-id="d450e-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




