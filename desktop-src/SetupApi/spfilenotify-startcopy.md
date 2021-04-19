---
description: La \_ notification SPFILENOTIFY STARTCOPY est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de copie de fichiers.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: Message d’SPFILENOTIFY_STARTCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529356"
---
# <a name="spfilenotify_startcopy-message"></a><span data-ttu-id="1503b-103">\_Message SPFILENOTIFY STARTCOPY</span><span class="sxs-lookup"><span data-stu-id="1503b-103">SPFILENOTIFY\_STARTCOPY message</span></span>

<span data-ttu-id="1503b-104">La notification **SPFILENOTIFY \_ STARTCOPY** est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1503b-104">The **SPFILENOTIFY\_STARTCOPY** notification is sent to the callback function when the queue starts a file copy operation.</span></span>


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="1503b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1503b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1503b-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="1503b-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="1503b-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="1503b-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1503b-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="1503b-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="1503b-109">A toujours la valeur FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="1503b-109">Always has the value FILEOP\_COPY.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1503b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1503b-110">Return value</span></span>

<span data-ttu-id="1503b-111">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1503b-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="1503b-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1503b-112">Return code</span></span>                                                                                  | <span data-ttu-id="1503b-113">Description</span><span class="sxs-lookup"><span data-stu-id="1503b-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1503b-114"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="1503b-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="1503b-115">Abandonner le processus de validation de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1503b-115">Abort the queue commit process.</span></span> <span data-ttu-id="1503b-116">La routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour indiquer la raison de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="1503b-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="1503b-117">La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel lors de l’appel à **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="1503b-117">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="1503b-118"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="1503b-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="1503b-119">Effectuez l’opération de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1503b-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1503b-120"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="1503b-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="1503b-121">Ignorer l’opération de copie en cours.</span><span class="sxs-lookup"><span data-stu-id="1503b-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="1503b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1503b-122">Requirements</span></span>



| <span data-ttu-id="1503b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1503b-123">Requirement</span></span> | <span data-ttu-id="1503b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1503b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1503b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1503b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1503b-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1503b-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1503b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1503b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1503b-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1503b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1503b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1503b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1503b-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1503b-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1503b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1503b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1503b-132">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="1503b-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="1503b-133">Notifications</span><span class="sxs-lookup"><span data-stu-id="1503b-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="1503b-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="1503b-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="1503b-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="1503b-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="1503b-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="1503b-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

