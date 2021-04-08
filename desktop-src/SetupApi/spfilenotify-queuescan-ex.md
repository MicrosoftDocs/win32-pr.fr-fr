---
description: La \_ notification SPFILENOTIFY QUEUESCAN \_ ex est envoyée à une routine de rappel par SetupScanFileQueue pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Message d’SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864190"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="cd7d7-103">\_Message SPFILENOTIFY QUEUESCAN \_ ex</span><span class="sxs-lookup"><span data-stu-id="cd7d7-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="cd7d7-104">La notification **SPFILENOTIFY \_ QUEUESCAN \_ ex** est envoyée à une routine de rappel par [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="cd7d7-105">Cela se produit uniquement si la fonction **SetupScanFileQueue** a été appelée en spécifiant l’indicateur SPQ \_ Scan \_ use \_ CALLBACKEX.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="cd7d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd7d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7d7-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="cd7d7-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7d7-108">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="cd7d7-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="cd7d7-109">Le membre **cible** est le nom du fichier cible sur le système.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="cd7d7-110">Le membre **source** est le chemin d’accès attendu du fichier source.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="cd7d7-111">Le membre **Win32Error** est l’erreur de signature.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7d7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd7d7-112">Return value</span></span>

<span data-ttu-id="cd7d7-113">La routine de rappel doit retourner un [code d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cd7d7-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="cd7d7-114">Si la routine de rappel ne retourne aucune \_ erreur, l’analyse de la file d’attente continue.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="cd7d7-115">Si la routine retourne un autre code d’erreur, l’analyse de la file d’attente s’interrompt et [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retourne false.</span><span class="sxs-lookup"><span data-stu-id="cd7d7-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="cd7d7-116">Cette notification n’est pas gérée par la fonction [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="cd7d7-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cd7d7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd7d7-117">Requirements</span></span>



| <span data-ttu-id="cd7d7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd7d7-118">Requirement</span></span> | <span data-ttu-id="cd7d7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd7d7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7d7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd7d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7d7-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd7d7-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd7d7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd7d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7d7-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd7d7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd7d7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd7d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd7d7-125"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd7d7-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7d7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd7d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7d7-127">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="cd7d7-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="cd7d7-128">Notifications</span><span class="sxs-lookup"><span data-stu-id="cd7d7-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="cd7d7-129">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="cd7d7-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

