---
description: Arrête le mode récepteur Miracast, désactive la détectabilité et annule l’inscription du rappel.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: WFDDisplaySinkStop, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531847"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="4322c-103">WFDDisplaySinkStop fonction)</span><span class="sxs-lookup"><span data-stu-id="4322c-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="4322c-104">Arrête le mode récepteur Miracast, désactive la détectabilité et annule l’inscription du rappel.</span><span class="sxs-lookup"><span data-stu-id="4322c-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="4322c-105">Votre application doit l’appeler une fois à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4322c-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="4322c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4322c-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="4322c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4322c-107">Parameters</span></span>

<span data-ttu-id="4322c-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4322c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4322c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4322c-109">Return value</span></span>

<span data-ttu-id="4322c-110">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="4322c-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="4322c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4322c-111">Remarks</span></span>

<span data-ttu-id="4322c-112">Il est prévu que votre application ait débloqué tous les rappels en cours avant d’appeler **WFDStopDisplaySink**.</span><span class="sxs-lookup"><span data-stu-id="4322c-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4322c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4322c-113">Requirements</span></span>



| <span data-ttu-id="4322c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4322c-114">Requirement</span></span> | <span data-ttu-id="4322c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4322c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4322c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4322c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4322c-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4322c-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4322c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4322c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4322c-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4322c-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4322c-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4322c-120">End of client support</span></span><br/>    | <span data-ttu-id="4322c-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4322c-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="4322c-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4322c-122">End of server support</span></span><br/>    | <span data-ttu-id="4322c-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4322c-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="4322c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4322c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4322c-125"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="4322c-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="4322c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4322c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4322c-127"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4322c-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="4322c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4322c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4322c-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4322c-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




