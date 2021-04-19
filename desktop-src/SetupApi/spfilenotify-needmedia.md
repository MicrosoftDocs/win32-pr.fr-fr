---
description: La \_ notification SPFILENOTIFY NEEDMEDIA est envoyée à la routine de rappel quand un nouveau média ou un nouveau fichier cab est requis.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Message d’SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523751"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="26ef3-103">\_Message SPFILENOTIFY NEEDMEDIA</span><span class="sxs-lookup"><span data-stu-id="26ef3-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="26ef3-104">La notification **SPFILENOTIFY \_ NEEDMEDIA** est envoyée à la routine de rappel quand un nouveau média ou un nouveau fichier cab est requis.</span><span class="sxs-lookup"><span data-stu-id="26ef3-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="26ef3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26ef3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ef3-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="26ef3-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="26ef3-107">Pointeur vers une structure de [**\_ média source**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .</span><span class="sxs-lookup"><span data-stu-id="26ef3-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="26ef3-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="26ef3-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="26ef3-109">Pointeur vers un tableau de caractères pour stocker les informations de chemin d’accès fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="26ef3-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="26ef3-110">La taille de la mémoire tampon est un tableau **TCHAR** d' \_ éléments de chemin d’accès max.</span><span class="sxs-lookup"><span data-stu-id="26ef3-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="26ef3-111">Les informations de chemin d’accès retournées par votre application d’installation ne doivent pas dépasser cette taille.</span><span class="sxs-lookup"><span data-stu-id="26ef3-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ef3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26ef3-112">Return value</span></span>

<span data-ttu-id="26ef3-113">La routine de rappel doit retourner l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="26ef3-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="26ef3-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="26ef3-114">Return code</span></span>                                                                                    | <span data-ttu-id="26ef3-115">Description</span><span class="sxs-lookup"><span data-stu-id="26ef3-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26ef3-116"><dt>**FILEOP \_ NewPath**</dt></span><span class="sxs-lookup"><span data-stu-id="26ef3-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="26ef3-117">Le média est présent et le fichier demandé est disponible dans le chemin d’accès spécifié dans la mémoire tampon pointée par *param2*.</span><span class="sxs-lookup"><span data-stu-id="26ef3-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="26ef3-118"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="26ef3-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="26ef3-119">Ignorer le fichier demandé</span><span class="sxs-lookup"><span data-stu-id="26ef3-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="26ef3-120"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="26ef3-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="26ef3-121">Abandon du traitement de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="26ef3-121">Abort queue processing.</span></span> <span data-ttu-id="26ef3-122">La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="26ef3-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="26ef3-123">GetLastError retourne des informations d’erreur étendues, telles que \_ l’erreur annulée si l’utilisateur a annulé.</span><span class="sxs-lookup"><span data-stu-id="26ef3-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="26ef3-124"><dt>**FILEOP-DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="26ef3-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="26ef3-125">Le média est disponible.</span><span class="sxs-lookup"><span data-stu-id="26ef3-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="26ef3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ef3-126">Requirements</span></span>



| <span data-ttu-id="26ef3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ef3-127">Requirement</span></span> | <span data-ttu-id="26ef3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ef3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26ef3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ef3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="26ef3-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ef3-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="26ef3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ef3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="26ef3-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ef3-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26ef3-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="26ef3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ef3-134"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ef3-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ef3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ef3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ef3-136">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="26ef3-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="26ef3-137">Notifications</span><span class="sxs-lookup"><span data-stu-id="26ef3-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="26ef3-138">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="26ef3-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="26ef3-139">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="26ef3-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="26ef3-140">**\_média source**</span><span class="sxs-lookup"><span data-stu-id="26ef3-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




