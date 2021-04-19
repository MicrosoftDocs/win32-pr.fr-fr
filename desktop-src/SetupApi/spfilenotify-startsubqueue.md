---
description: La \_ notification SPFILENOTIFY STARTSUBQUEUE est envoyée à la fonction de rappel lorsque la file d’attente commence à traiter les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Message d’SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522207"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="5a7ac-103">\_Message SPFILENOTIFY STARTSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="5a7ac-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="5a7ac-104">La notification **SPFILENOTIFY \_ STARTSUBQUEUE** est envoyée à la fonction de rappel lorsque la file d’attente commence à traiter les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="5a7ac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a7ac-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a7ac-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="5a7ac-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7ac-107">Sous-file d’attente qui a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-107">Subqueue that has been started.</span></span> <span data-ttu-id="5a7ac-108">Ce paramètre peut prendre l’une des valeurs FILEOP \_ Delete, FILEOP \_ Rename ou FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="5a7ac-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="5a7ac-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7ac-110">Nombre d’opérations de copie, de renommage ou de suppression de fichiers dans la sous-file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a7ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a7ac-111">Return value</span></span>

<span data-ttu-id="5a7ac-112">Si une erreur se produit, la routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), en spécifiant l’erreur, puis retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="5a7ac-113">La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="5a7ac-114">Si aucune erreur ne se produit, la routine de rappel doit retourner une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5a7ac-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a7ac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a7ac-115">Requirements</span></span>



| <span data-ttu-id="5a7ac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a7ac-116">Requirement</span></span> | <span data-ttu-id="5a7ac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a7ac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a7ac-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a7ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a7ac-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a7ac-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5a7ac-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a7ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a7ac-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a7ac-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a7ac-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a7ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a7ac-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a7ac-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a7ac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a7ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7ac-125">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="5a7ac-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="5a7ac-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="5a7ac-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="5a7ac-127">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="5a7ac-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="5a7ac-128">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="5a7ac-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

