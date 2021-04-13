---
description: La \_ notification SPFILENOTIFY RENAMEERROR est envoyée à la routine de rappel si une erreur se produit pendant une opération de changement de nom de fichier.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Message d’SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319874"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="fa880-103">\_Message SPFILENOTIFY RENAMEERROR</span><span class="sxs-lookup"><span data-stu-id="fa880-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="fa880-104">La notification **SPFILENOTIFY \_ RENAMEERROR** est envoyée à la routine de rappel si une erreur se produit pendant une opération de changement de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="fa880-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="fa880-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa880-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa880-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="fa880-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="fa880-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="fa880-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="fa880-108">Le membre **Win32Error** de la structure **FILEPATHS** spécifie l’erreur qui s’est produite pendant l’opération de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="fa880-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="fa880-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="fa880-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="fa880-110">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="fa880-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa880-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa880-111">Return value</span></span>

<span data-ttu-id="fa880-112">La routine de rappel doit retourner l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="fa880-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="fa880-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fa880-113">Return code</span></span>                                                                                  | <span data-ttu-id="fa880-114">Description</span><span class="sxs-lookup"><span data-stu-id="fa880-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa880-115"><dt>**\_nouvelle tentative FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="fa880-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="fa880-116">L’utilisateur a choisi de retenter l’opération de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="fa880-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="fa880-117"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="fa880-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="fa880-118">L’utilisateur a choisi d’ignorer l’opération de changement de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="fa880-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="fa880-119"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="fa880-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="fa880-120">Arrêtez la validation de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fa880-120">Stop the queue commit.</span></span> <span data-ttu-id="fa880-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fa880-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="fa880-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne des informations d’erreur étendues, telles que \_ l’erreur annulée (si l’utilisateur a annulé) ou une erreur de \_ \_ mémoire insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="fa880-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa880-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa880-123">Requirements</span></span>



| <span data-ttu-id="fa880-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa880-124">Requirement</span></span> | <span data-ttu-id="fa880-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa880-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa880-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa880-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa880-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa880-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa880-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa880-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa880-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa880-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa880-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa880-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa880-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa880-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa880-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa880-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa880-133">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="fa880-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="fa880-134">Notifications</span><span class="sxs-lookup"><span data-stu-id="fa880-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="fa880-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="fa880-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="fa880-136">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="fa880-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="fa880-137">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="fa880-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

