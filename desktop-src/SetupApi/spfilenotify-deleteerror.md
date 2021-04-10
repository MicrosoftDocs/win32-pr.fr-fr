---
description: La \_ notification SPFILENOTIFY DELETEERROR est envoyée à la routine de rappel si une erreur se produit pendant une opération de suppression de fichier.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Message d’SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042768"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="db9d8-103">\_Message SPFILENOTIFY DELETEERROR</span><span class="sxs-lookup"><span data-stu-id="db9d8-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="db9d8-104">La notification **SPFILENOTIFY \_ DELETEERROR** est envoyée à la routine de rappel si une erreur se produit pendant une opération de suppression de fichier.</span><span class="sxs-lookup"><span data-stu-id="db9d8-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="db9d8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db9d8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9d8-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="db9d8-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="db9d8-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="db9d8-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="db9d8-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="db9d8-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="db9d8-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="db9d8-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9d8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db9d8-110">Return value</span></span>

<span data-ttu-id="db9d8-111">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="db9d8-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="db9d8-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="db9d8-112">Return code</span></span>                                                                                  | <span data-ttu-id="db9d8-113">Description</span><span class="sxs-lookup"><span data-stu-id="db9d8-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db9d8-114"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="db9d8-115">Le traitement de la file d’attente doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="db9d8-115">Queue processing should be canceled.</span></span> <span data-ttu-id="db9d8-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne zéro et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne des informations d’erreur étendues, telles que \_ l’erreur annulée (si l’utilisateur a annulé) ou une erreur de \_ \_ mémoire insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="db9d8-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="db9d8-117"><dt>**\_nouvelle tentative FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="db9d8-118">L’utilisateur tente à nouveau l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="db9d8-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="db9d8-119"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="db9d8-120">L’utilisateur ignore l’opération de suppression de fichier.</span><span class="sxs-lookup"><span data-stu-id="db9d8-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="db9d8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db9d8-121">Requirements</span></span>



| <span data-ttu-id="db9d8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db9d8-122">Requirement</span></span> | <span data-ttu-id="db9d8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="db9d8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db9d8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db9d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="db9d8-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db9d8-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="db9d8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db9d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="db9d8-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db9d8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db9d8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="db9d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9d8-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9d8-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db9d8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db9d8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9d8-131">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="db9d8-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="db9d8-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="db9d8-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="db9d8-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="db9d8-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="db9d8-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="db9d8-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="db9d8-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="db9d8-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

