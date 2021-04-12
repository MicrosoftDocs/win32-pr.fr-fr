---
description: La \_ notification SPFILENOTIFY NEEDNEWCABINET est envoyée par SetupIterateCabinet pour indiquer que le fichier actuel continue dans une autre armoire.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Message d’SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210423"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="97e54-103">\_Message SPFILENOTIFY NEEDNEWCABINET</span><span class="sxs-lookup"><span data-stu-id="97e54-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="97e54-104">La notification **SPFILENOTIFY \_ NEEDNEWCABINET** est envoyée par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour indiquer que le fichier actuel continue dans une autre armoire.</span><span class="sxs-lookup"><span data-stu-id="97e54-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="97e54-105">Votre routine de rappel peut ensuite appeler [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)ou créer sa propre boîte de dialogue pour inviter l’utilisateur à insérer le disque suivant.</span><span class="sxs-lookup"><span data-stu-id="97e54-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="97e54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e54-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="97e54-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="97e54-108">Pointeur vers une structure d' [**\_ informations d’armoire**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) qui contient des informations sur l’armoire et le fichier à extraire.</span><span class="sxs-lookup"><span data-stu-id="97e54-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="97e54-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="97e54-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="97e54-110">Si le rappel ne retourne aucune \_ erreur, ce paramètre est un pointeur vers une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="97e54-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="97e54-111">Si la chaîne n’est pas vide, elle spécifie un nouveau chemin d’accès au fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="97e54-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e54-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97e54-112">Return value</span></span>

<span data-ttu-id="97e54-113">Votre routine doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="97e54-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="97e54-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="97e54-114">Return code</span></span>                                                                                 | <span data-ttu-id="97e54-115">Description</span><span class="sxs-lookup"><span data-stu-id="97e54-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97e54-116"><dt>**AUCUNE \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="97e54-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="97e54-117">Aucune erreur ne s’est produite. poursuivez le traitement du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="97e54-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="97e54-118"><dt>\**Erreur \_* XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="97e54-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="97e54-119">Une erreur du type spécifié s’est produite.</span><span class="sxs-lookup"><span data-stu-id="97e54-119">An error of the specified type occurred.</span></span> <span data-ttu-id="97e54-120">La fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retourne la **valeur false** et le code d’erreur spécifié est retourné par un appel à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="97e54-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="97e54-121">Il n’existe aucune routine de rappel d’armoire par défaut ; par conséquent, vous devez fournir une routine de rappel pour gérer les notifications envoyées par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="97e54-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="97e54-122">Notes</span><span class="sxs-lookup"><span data-stu-id="97e54-122">Remarks</span></span>

<span data-ttu-id="97e54-123">Si la routine de rappel ne retourne aucune \_ erreur, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) vérifie la mémoire tampon désignée par *param2*.</span><span class="sxs-lookup"><span data-stu-id="97e54-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="97e54-124">Si la mémoire tampon n’est pas vide, elle contient un nouveau chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="97e54-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="97e54-125">Si la mémoire tampon est vide, le chemin d’accès source est supposé être inchangé.</span><span class="sxs-lookup"><span data-stu-id="97e54-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="97e54-126">Votre fonction de rappel doit s’assurer que le fichier cab est accessible avant de retourner, en appelant la fonction [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , si un nouveau support doit être inséré.</span><span class="sxs-lookup"><span data-stu-id="97e54-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e54-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97e54-127">Requirements</span></span>



| <span data-ttu-id="97e54-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97e54-128">Requirement</span></span> | <span data-ttu-id="97e54-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="97e54-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97e54-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e54-130">Minimum supported client</span></span><br/> | <span data-ttu-id="97e54-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97e54-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97e54-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e54-132">Minimum supported server</span></span><br/> | <span data-ttu-id="97e54-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97e54-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97e54-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="97e54-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e54-135"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e54-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e54-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e54-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e54-137">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="97e54-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="97e54-138">Notifications</span><span class="sxs-lookup"><span data-stu-id="97e54-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="97e54-139">**\_infos sur le cabinet**</span><span class="sxs-lookup"><span data-stu-id="97e54-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="97e54-140">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="97e54-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

