---
description: Récupère le nombre de processeurs sur lesquels le thread actuel s’exécutait pendant l’appel à cette fonction.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533442"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="ac746-103">NtGetCurrentProcessorNumber fonction)</span><span class="sxs-lookup"><span data-stu-id="ac746-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="ac746-104">\[Les **NtGetCurrentProcessorNumber** peuvent être modifiés ou non disponibles dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="ac746-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="ac746-105">Les applications doivent utiliser la fonction [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="ac746-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="ac746-106">Récupère le nombre de processeurs sur lesquels le thread actuel s’exécutait pendant l’appel à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ac746-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac746-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac746-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="ac746-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac746-108">Parameters</span></span>

<span data-ttu-id="ac746-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ac746-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac746-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac746-110">Return value</span></span>

<span data-ttu-id="ac746-111">La fonction retourne le numéro de processeur actuel.</span><span class="sxs-lookup"><span data-stu-id="ac746-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac746-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ac746-112">Remarks</span></span>

<span data-ttu-id="ac746-113">Cette fonction est utilisée pour fournir des informations sur l’estimation des performances du processus.</span><span class="sxs-lookup"><span data-stu-id="ac746-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="ac746-114">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="ac746-114">This function has no associated import library.</span></span> <span data-ttu-id="ac746-115">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="ac746-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac746-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac746-116">Requirements</span></span>



| <span data-ttu-id="ac746-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac746-117">Requirement</span></span> | <span data-ttu-id="ac746-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac746-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac746-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ac746-119">DLL</span></span><br/> | <dl> <span data-ttu-id="ac746-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac746-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac746-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac746-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac746-122">Plusieurs processeurs</span><span class="sxs-lookup"><span data-stu-id="ac746-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="ac746-123">Fonctions de processus et de thread</span><span class="sxs-lookup"><span data-stu-id="ac746-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="ac746-124">Processus</span><span class="sxs-lookup"><span data-stu-id="ac746-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
