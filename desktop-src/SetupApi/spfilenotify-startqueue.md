---
description: La \_ notification SPFILENOTIFY STARTQUEUE est envoyée à la routine de rappel lors du démarrage du processus d’engagement de file d’attente.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Message d’SPFILENOTIFY_STARTQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537052"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="07761-103">\_Message SPFILENOTIFY STARTQUEUE</span><span class="sxs-lookup"><span data-stu-id="07761-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="07761-104">La notification **SPFILENOTIFY \_ STARTQUEUE** est envoyée à la routine de rappel lors du démarrage du processus d’engagement de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="07761-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="07761-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07761-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07761-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="07761-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="07761-107">Handle de la fenêtre qui doit posséder les boîtes de dialogue générées par la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="07761-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="07761-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="07761-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="07761-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="07761-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07761-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07761-110">Return value</span></span>

<span data-ttu-id="07761-111">Si une erreur se produit, la routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), en spécifiant l’erreur, puis retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="07761-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="07761-112">La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="07761-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="07761-113">Si aucune erreur ne se produit, la routine de rappel doit retourner une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="07761-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="07761-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07761-114">Requirements</span></span>



| <span data-ttu-id="07761-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07761-115">Requirement</span></span> | <span data-ttu-id="07761-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="07761-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07761-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07761-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07761-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07761-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="07761-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07761-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07761-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07761-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07761-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="07761-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07761-122"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="07761-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07761-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07761-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07761-124">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="07761-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="07761-125">Notifications</span><span class="sxs-lookup"><span data-stu-id="07761-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="07761-126">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="07761-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="07761-127">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="07761-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

