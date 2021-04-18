---
description: La \_ notification SPFILENOTIFY STARTRENAME est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de changement de nom de fichier.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: Message d’SPFILENOTIFY_STARTRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c17d0c70b49ba00b3b16956e7ede5eda43b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526201"
---
# <a name="spfilenotify_startrename-message"></a><span data-ttu-id="f6716-103">\_Message SPFILENOTIFY STARTRENAME</span><span class="sxs-lookup"><span data-stu-id="f6716-103">SPFILENOTIFY\_STARTRENAME message</span></span>

<span data-ttu-id="f6716-104">La notification **SPFILENOTIFY \_ STARTRENAME** est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de changement de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="f6716-104">The **SPFILENOTIFY\_STARTRENAME** notification is sent to the callback function when the queue starts a file rename operation.</span></span>


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="f6716-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6716-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6716-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="f6716-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f6716-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="f6716-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f6716-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f6716-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f6716-109">A toujours la valeur FILEOP \_ Rename.</span><span class="sxs-lookup"><span data-stu-id="f6716-109">Always has the value FILEOP\_RENAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6716-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6716-110">Return value</span></span>

<span data-ttu-id="f6716-111">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6716-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="f6716-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f6716-112">Return code</span></span>                                                                                  | <span data-ttu-id="f6716-113">Description</span><span class="sxs-lookup"><span data-stu-id="f6716-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6716-114"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="f6716-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="f6716-115">Abandonner la validation de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f6716-115">Abort the queue commit.</span></span> <span data-ttu-id="f6716-116">La routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour indiquer la raison de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f6716-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="f6716-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne **false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel lors de l’appel à **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="f6716-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="f6716-118"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="f6716-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="f6716-119">Effectuez l’opération de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f6716-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f6716-120"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="f6716-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="f6716-121">Ignorer l’opération de copie en cours.</span><span class="sxs-lookup"><span data-stu-id="f6716-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="f6716-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6716-122">Requirements</span></span>



| <span data-ttu-id="f6716-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6716-123">Requirement</span></span> | <span data-ttu-id="f6716-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6716-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6716-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6716-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f6716-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6716-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f6716-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6716-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f6716-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6716-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6716-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6716-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6716-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6716-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6716-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6716-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6716-132">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="f6716-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f6716-133">Notifications</span><span class="sxs-lookup"><span data-stu-id="f6716-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f6716-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="f6716-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="f6716-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="f6716-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="f6716-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="f6716-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

