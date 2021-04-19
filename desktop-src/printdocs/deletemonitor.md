---
description: La fonction DeleteMonitor supprime un moniteur de port ajouté par la fonction AddMonitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: DeleteMonitor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538884"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="aa921-103">DeleteMonitor fonction)</span><span class="sxs-lookup"><span data-stu-id="aa921-103">DeleteMonitor function</span></span>

<span data-ttu-id="aa921-104">La fonction **DeleteMonitor** supprime un moniteur de port ajouté par la fonction [**AddMonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="aa921-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa921-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa921-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="aa921-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa921-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa921-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa921-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel l’analyse doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="aa921-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="aa921-109">Si ce paramètre a la **valeur null**, le moniteur de port est supprimé localement.</span><span class="sxs-lookup"><span data-stu-id="aa921-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="aa921-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa921-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa921-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le moniteur doit être supprimé (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="aa921-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="aa921-112">Si ce paramètre a la **valeur null**, l’analyse est supprimée de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression).</span><span class="sxs-lookup"><span data-stu-id="aa921-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="aa921-113">*pMonitorName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa921-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa921-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’analyse à supprimer.</span><span class="sxs-lookup"><span data-stu-id="aa921-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa921-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa921-115">Return value</span></span>

<span data-ttu-id="aa921-116">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="aa921-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="aa921-117">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="aa921-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa921-118">Notes</span><span class="sxs-lookup"><span data-stu-id="aa921-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aa921-119">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="aa921-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="aa921-120">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="aa921-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="aa921-121">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="aa921-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="aa921-122">L’appelant doit avoir [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="aa921-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa921-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa921-123">Requirements</span></span>



| <span data-ttu-id="aa921-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa921-124">Requirement</span></span> | <span data-ttu-id="aa921-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa921-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa921-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa921-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aa921-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa921-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa921-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa921-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aa921-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa921-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa921-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa921-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa921-131"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa921-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="aa921-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aa921-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa921-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa921-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="aa921-134">DLL</span><span class="sxs-lookup"><span data-stu-id="aa921-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa921-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="aa921-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="aa921-136">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="aa921-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aa921-137">**DeleteMonitorW** (Unicode) et **DeleteMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aa921-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="aa921-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa921-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa921-139">Impression</span><span class="sxs-lookup"><span data-stu-id="aa921-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="aa921-140">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="aa921-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="aa921-141">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="aa921-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

