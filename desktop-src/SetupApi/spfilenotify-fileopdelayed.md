---
description: La \_ notification SPFILENOTIFY FILEOPDELAYED est envoyée par SetupInstallFileEx ou SetupCommitFileQueue à une routine de rappel lorsqu’une opération de fichier a été retardée parce que le fichier était en cours d’utilisation. L’opération sera traitée lors du prochain redémarrage du système.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Message d’SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864193"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="83c42-104">\_Message SPFILENOTIFY FILEOPDELAYED</span><span class="sxs-lookup"><span data-stu-id="83c42-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="83c42-105">La notification **SPFILENOTIFY \_ FILEOPDELAYED** est envoyée par [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) ou [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) à une routine de rappel lorsqu’une opération de fichier a été retardée parce que le fichier était en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="83c42-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="83c42-106">L’opération sera traitée lors du prochain redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="83c42-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="83c42-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83c42-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c42-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="83c42-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="83c42-109">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="83c42-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="83c42-110">Si l’opération retardée est une opération de copie de fichier, la structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="83c42-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="83c42-111">Membre FILEPATHS</span><span class="sxs-lookup"><span data-stu-id="83c42-111">FILEPATHS member</span></span> | <span data-ttu-id="83c42-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c42-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="83c42-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="83c42-113">**Win32Error**</span></span>   | <span data-ttu-id="83c42-114">AUCUNE \_ erreur</span><span class="sxs-lookup"><span data-stu-id="83c42-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="83c42-115">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="83c42-115">**Flags**</span></span>        | <span data-ttu-id="83c42-116">\_copie FILEOP</span><span class="sxs-lookup"><span data-stu-id="83c42-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="83c42-117">**Source**</span><span class="sxs-lookup"><span data-stu-id="83c42-117">**Source**</span></span>       | <span data-ttu-id="83c42-118">Chemin d’accès complet du fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="83c42-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="83c42-119">**Cible**</span><span class="sxs-lookup"><span data-stu-id="83c42-119">**Target**</span></span>       | <span data-ttu-id="83c42-120">Chemin d’accès complet du fichier cible réel.</span><span class="sxs-lookup"><span data-stu-id="83c42-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="83c42-121">Ce fichier temporaire sera copié dans le répertoire cible lors du redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="83c42-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="83c42-122">Les fonctions de configuration génèrent automatiquement un chemin d’accès pour le fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="83c42-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="83c42-123">Si l’opération retardée est une opération de suppression de fichier, la structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="83c42-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="83c42-124">Membre FILEPATHS</span><span class="sxs-lookup"><span data-stu-id="83c42-124">FILEPATHS member</span></span> | <span data-ttu-id="83c42-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c42-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="83c42-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="83c42-126">**Win32Error**</span></span>   | <span data-ttu-id="83c42-127">AUCUNE \_ erreur</span><span class="sxs-lookup"><span data-stu-id="83c42-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="83c42-128">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="83c42-128">**Flags**</span></span>        | <span data-ttu-id="83c42-129">FILEOP \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="83c42-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="83c42-130">**Source**</span><span class="sxs-lookup"><span data-stu-id="83c42-130">**Source**</span></span>       | <span data-ttu-id="83c42-131">NULL</span><span class="sxs-lookup"><span data-stu-id="83c42-131">NULL</span></span>                                 |
| <span data-ttu-id="83c42-132">**Cible**</span><span class="sxs-lookup"><span data-stu-id="83c42-132">**Target**</span></span>       | <span data-ttu-id="83c42-133">Chemin d’accès complet du fichier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="83c42-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="83c42-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="83c42-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="83c42-135">N'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="83c42-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c42-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83c42-136">Return value</span></span>

<span data-ttu-id="83c42-137">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="83c42-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c42-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83c42-138">Requirements</span></span>



| <span data-ttu-id="83c42-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83c42-139">Requirement</span></span> | <span data-ttu-id="83c42-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c42-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83c42-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c42-141">Minimum supported client</span></span><br/> | <span data-ttu-id="83c42-142">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83c42-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="83c42-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c42-143">Minimum supported server</span></span><br/> | <span data-ttu-id="83c42-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83c42-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83c42-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="83c42-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c42-146"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c42-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c42-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83c42-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c42-148">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="83c42-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="83c42-149">Notifications</span><span class="sxs-lookup"><span data-stu-id="83c42-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="83c42-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="83c42-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="83c42-151">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="83c42-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="83c42-152">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="83c42-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="83c42-153">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="83c42-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="83c42-154">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="83c42-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




