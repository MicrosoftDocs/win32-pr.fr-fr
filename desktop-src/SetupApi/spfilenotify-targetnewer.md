---
description: La \_ notification SPFILENOTIFY TARGETNEWER est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec les indicateurs plus récents de la \_ copie SP \_ plus récente ou de la \_ copie SP \_ \_ , et qu’une version plus récente du fichier existe déjà dans le répertoire cible.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Message d’SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542948"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="6888a-103">\_Message SPFILENOTIFY TARGETNEWER</span><span class="sxs-lookup"><span data-stu-id="6888a-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="6888a-104">La notification **SPFILENOTIFY \_ TARGETNEWER** est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec les indicateurs plus récents de la \_ copie SP \_ plus récente ou de la \_ copie SP \_ \_ , et qu’une version plus récente du fichier existe déjà dans le répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="6888a-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="6888a-105">Elle peut être envoyée à la routine de rappel seule ou associée à [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) et/ou [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).</span><span class="sxs-lookup"><span data-stu-id="6888a-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="6888a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6888a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6888a-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="6888a-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="6888a-108">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations sur les chemins d’accès pour les fichiers source et cible.</span><span class="sxs-lookup"><span data-stu-id="6888a-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="6888a-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="6888a-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="6888a-110">Ce paramètre n’est pas utilisé, sauf si cette notification est combinée, à l’aide de l’opérateur OR, avec [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).</span><span class="sxs-lookup"><span data-stu-id="6888a-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6888a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6888a-111">Return value</span></span>

<span data-ttu-id="6888a-112">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6888a-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="6888a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6888a-113">Return code</span></span>                                                                          | <span data-ttu-id="6888a-114">Description</span><span class="sxs-lookup"><span data-stu-id="6888a-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="6888a-115"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="6888a-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="6888a-116">Remplacez le fichier dans le répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="6888a-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="6888a-117"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="6888a-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="6888a-118">Ignorer l’opération de copie en cours.</span><span class="sxs-lookup"><span data-stu-id="6888a-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="6888a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6888a-119">Requirements</span></span>



| <span data-ttu-id="6888a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6888a-120">Requirement</span></span> | <span data-ttu-id="6888a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6888a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6888a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6888a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6888a-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6888a-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6888a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6888a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6888a-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6888a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6888a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6888a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6888a-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6888a-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6888a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6888a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6888a-129">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="6888a-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="6888a-130">Notifications</span><span class="sxs-lookup"><span data-stu-id="6888a-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="6888a-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="6888a-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="6888a-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="6888a-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="6888a-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="6888a-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="6888a-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="6888a-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="6888a-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="6888a-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="6888a-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="6888a-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




