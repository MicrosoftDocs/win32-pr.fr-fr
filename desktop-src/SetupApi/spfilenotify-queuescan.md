---
description: La \_ notification SPFILENOTIFY QUEUESCAN est envoyée à une routine de rappel par SetupScanFileQueue pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers. Cela se produit uniquement si la fonction SetupScanFileQueue a été appelée en spécifiant le rappel d’utilisation de l’indicateur SPQ \_ Scan \_ \_ .
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Message d’SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530154"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="aaff9-104">\_Message SPFILENOTIFY QUEUESCAN</span><span class="sxs-lookup"><span data-stu-id="aaff9-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="aaff9-105">La notification **SPFILENOTIFY \_ QUEUESCAN** est envoyée à une routine de rappel par [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="aaff9-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="aaff9-106">Cela se produit uniquement si la fonction **SetupScanFileQueue** a été appelée en spécifiant le rappel d’utilisation de l’indicateur SPQ \_ Scan \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aaff9-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="aaff9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaff9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaff9-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="aaff9-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="aaff9-109">Chaîne terminée par le caractère null qui spécifie les informations de chemin d’accès cible pour le fichier mis en file d’attente dans le nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="aaff9-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="aaff9-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="aaff9-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="aaff9-111">Si le fichier du nœud actuel de la file d’attente est en cours d’utilisation, *param2* prend la valeur SPQ \_ retardée \_ .</span><span class="sxs-lookup"><span data-stu-id="aaff9-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="aaff9-112">Si le fichier n’est pas utilisé, la valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="aaff9-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaff9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aaff9-113">Return value</span></span>

<span data-ttu-id="aaff9-114">La routine de rappel doit retourner un [code d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="aaff9-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="aaff9-115">Si la routine de rappel ne retourne aucune \_ erreur, l’analyse de la file d’attente continue.</span><span class="sxs-lookup"><span data-stu-id="aaff9-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="aaff9-116">Si la routine retourne un autre code d’erreur, l’analyse de la file d’attente s’interrompt et [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="aaff9-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="aaff9-117">Cette notification n’est pas gérée par la fonction [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="aaff9-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aaff9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaff9-118">Requirements</span></span>



| <span data-ttu-id="aaff9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaff9-119">Requirement</span></span> | <span data-ttu-id="aaff9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaff9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aaff9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaff9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aaff9-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aaff9-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aaff9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaff9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aaff9-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aaff9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aaff9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaff9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaff9-126"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaff9-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaff9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaff9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaff9-128">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="aaff9-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="aaff9-129">Notifications</span><span class="sxs-lookup"><span data-stu-id="aaff9-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="aaff9-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="aaff9-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

