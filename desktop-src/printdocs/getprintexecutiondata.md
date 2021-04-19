---
description: Le GetPrintExecutionData récupère le contexte d’impression actuel.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: GetPrintExecutionData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542007"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="21c52-103">GetPrintExecutionData fonction)</span><span class="sxs-lookup"><span data-stu-id="21c52-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="21c52-104">Le **GetPrintExecutionData** récupère le contexte d’impression actuel.</span><span class="sxs-lookup"><span data-stu-id="21c52-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="21c52-105">Cette fonction est destinée à être utilisée par les pilotes d’imprimante qui s’exécutent dans le contexte du spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="21c52-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="21c52-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21c52-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="21c52-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21c52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c52-108">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="21c52-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21c52-109">Pointeur vers une variable qui reçoit l’adresse de la structure [**de \_ \_ données d’exécution**](print-execution-data.md) de l’impression.</span><span class="sxs-lookup"><span data-stu-id="21c52-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21c52-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21c52-110">Return value</span></span>

<span data-ttu-id="21c52-111">Retourne la **valeur true** si la fonction est réussie ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="21c52-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="21c52-112">Si la valeur de retour est **false**, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir l’état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="21c52-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="21c52-113">Notes</span><span class="sxs-lookup"><span data-stu-id="21c52-113">Remarks</span></span>

<span data-ttu-id="21c52-114">Les pilotes d’imprimante doivent appeler [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) sur le module winspool. drv pour récupérer l’adresse de la fonction **GetPrintExecutionData** , car **GetPrintExecutionData** n’est pas pris en charge sur Windows Vista ou les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="21c52-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="21c52-115">**GetPrintExecutionData** échoue uniquement si la valeur de *pData* est **null**.</span><span class="sxs-lookup"><span data-stu-id="21c52-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="21c52-116">La valeur du membre **clientAppPID** des [**données d' \_ exécution \_**](print-execution-data.md) de l’impression n’est significative que si la valeur de **Context** est le **contexte d’exécution d’impression \_ \_ \_ WOW64**.</span><span class="sxs-lookup"><span data-stu-id="21c52-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="21c52-117">Si la valeur du **contexte** n’affiche pas le **\_ contexte d’exécution \_ \_ WOW64**, la valeur de **clientAppPID** est 0.</span><span class="sxs-lookup"><span data-stu-id="21c52-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="21c52-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21c52-118">Requirements</span></span>



| <span data-ttu-id="21c52-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21c52-119">Requirement</span></span> | <span data-ttu-id="21c52-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="21c52-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21c52-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21c52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21c52-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21c52-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="21c52-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21c52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21c52-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21c52-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="21c52-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="21c52-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="21c52-126"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21c52-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="21c52-127">DLL</span><span class="sxs-lookup"><span data-stu-id="21c52-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21c52-128"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="21c52-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="21c52-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21c52-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c52-130">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="21c52-130">**GetLastError**</span></span>](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="21c52-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="21c52-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="21c52-132">**Imprimer \_ le \_ contexte d’exécution**</span><span class="sxs-lookup"><span data-stu-id="21c52-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="21c52-133">**Imprimer \_ les \_ données d’exécution**</span><span class="sxs-lookup"><span data-stu-id="21c52-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

