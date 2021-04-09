---
description: La \_ notification SPFILENOTIFY COPYERROR est envoyée à la routine de rappel si une erreur se produit pendant une opération de copie de fichier.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Message d’SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865714"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="400cd-103">\_Message SPFILENOTIFY COPYERROR</span><span class="sxs-lookup"><span data-stu-id="400cd-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="400cd-104">La notification **SPFILENOTIFY \_ COPYERROR** est envoyée à la routine de rappel si une erreur se produit pendant une opération de copie de fichier.</span><span class="sxs-lookup"><span data-stu-id="400cd-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="400cd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="400cd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="400cd-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="400cd-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="400cd-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="400cd-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="400cd-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="400cd-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="400cd-109">Pointeur vers une mémoire tampon, de taille maximale de caractères de chemin d’accès \_ , qui stocke les informations de chemin d’accès spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="400cd-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="400cd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="400cd-110">Return value</span></span>

<span data-ttu-id="400cd-111">Le rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="400cd-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="400cd-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="400cd-112">Return code</span></span>                                                                                    | <span data-ttu-id="400cd-113">Description</span><span class="sxs-lookup"><span data-stu-id="400cd-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="400cd-114"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="400cd-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="400cd-115">Le traitement de la file d’attente doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="400cd-115">Queue processing should be canceled.</span></span> <span data-ttu-id="400cd-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne zéro et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne des informations d’erreur étendues, telles que \_ l’erreur annulée (si l’utilisateur a annulé) ou une erreur de \_ \_ mémoire insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="400cd-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="400cd-117"><dt>**FILEOP \_ NewPath**</dt></span><span class="sxs-lookup"><span data-stu-id="400cd-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="400cd-118">Recommencez l’opération de copie à l’aide du chemin d’accès de la fonction de rappel placée dans la mémoire tampon vers laquelle pointe le paramètre *param2* .</span><span class="sxs-lookup"><span data-stu-id="400cd-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="400cd-119">La routine de rappel doit garantir que le chemin d’accès ne dépasse pas la taille de la mémoire tampon d’un tableau TCHAR d' \_ éléments de chemin d’accès max.</span><span class="sxs-lookup"><span data-stu-id="400cd-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="400cd-120"><dt>**\_nouvelle tentative FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="400cd-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="400cd-121">L’utilisateur tente à nouveau l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="400cd-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="400cd-122"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="400cd-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="400cd-123">L’utilisateur ignore l’opération de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="400cd-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="400cd-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="400cd-124">Requirements</span></span>



| <span data-ttu-id="400cd-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="400cd-125">Requirement</span></span> | <span data-ttu-id="400cd-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="400cd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="400cd-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="400cd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="400cd-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="400cd-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="400cd-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="400cd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="400cd-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="400cd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="400cd-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="400cd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="400cd-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="400cd-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="400cd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="400cd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400cd-134">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="400cd-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="400cd-135">Notifications</span><span class="sxs-lookup"><span data-stu-id="400cd-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="400cd-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="400cd-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="400cd-137">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="400cd-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="400cd-138">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="400cd-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

