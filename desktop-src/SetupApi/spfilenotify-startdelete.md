---
description: La \_ notification SPFILENOTIFY STARTDELETE est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de suppression de fichier.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: Message d’SPFILENOTIFY_STARTDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a4a0d362a1c1c3824154fb02e0bb9cf01b24d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529770"
---
# <a name="spfilenotify_startdelete-message"></a><span data-ttu-id="84781-103">\_Message SPFILENOTIFY STARTDELETE</span><span class="sxs-lookup"><span data-stu-id="84781-103">SPFILENOTIFY\_STARTDELETE message</span></span>

<span data-ttu-id="84781-104">La notification **SPFILENOTIFY \_ STARTDELETE** est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de suppression de fichier.</span><span class="sxs-lookup"><span data-stu-id="84781-104">The **SPFILENOTIFY\_STARTDELETE** notification is sent to the callback function when the queue starts a file delete operation.</span></span>


```C++
SPFILENOTIFY_STARTDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="84781-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84781-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84781-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="84781-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="84781-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="84781-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="84781-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="84781-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="84781-109">A toujours la valeur FILEOP \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="84781-109">Always has the value FILEOP\_DELETE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84781-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84781-110">Return value</span></span>

<span data-ttu-id="84781-111">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="84781-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="84781-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="84781-112">Return code</span></span>                                                                                  | <span data-ttu-id="84781-113">Description</span><span class="sxs-lookup"><span data-stu-id="84781-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84781-114"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="84781-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="84781-115">Abandonner la validation de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="84781-115">Abort the queue commit.</span></span> <span data-ttu-id="84781-116">La routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour indiquer la raison de l’abandon.</span><span class="sxs-lookup"><span data-stu-id="84781-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for aborting.</span></span> <span data-ttu-id="84781-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne **false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel lors de l’appel à **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="84781-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="84781-118"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="84781-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="84781-119">Effectuez l’opération de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="84781-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="84781-120"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="84781-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="84781-121">Ignorer l’opération de copie en cours.</span><span class="sxs-lookup"><span data-stu-id="84781-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="84781-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84781-122">Requirements</span></span>



| <span data-ttu-id="84781-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84781-123">Requirement</span></span> | <span data-ttu-id="84781-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="84781-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84781-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84781-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84781-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84781-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84781-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84781-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84781-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84781-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84781-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="84781-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="84781-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="84781-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84781-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84781-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84781-132">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="84781-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="84781-133">Notifications</span><span class="sxs-lookup"><span data-stu-id="84781-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="84781-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="84781-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="84781-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="84781-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="84781-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="84781-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

