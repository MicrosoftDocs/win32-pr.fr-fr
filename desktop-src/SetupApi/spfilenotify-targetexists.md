---
description: La \_ notification SPFILENOTIFY TARGETEXISTS est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec l' \_ indicateur SP Copy \_ NOOVERWRITE et que ce fichier existe déjà dans le répertoire cible.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Message d’SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393715"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="adf6f-103">\_Message SPFILENOTIFY TARGETEXISTS</span><span class="sxs-lookup"><span data-stu-id="adf6f-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="adf6f-104">La notification **SPFILENOTIFY \_ TARGETEXISTS** est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec l' \_ indicateur SP Copy \_ NOOVERWRITE et que ce fichier existe déjà dans le répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="adf6f-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="adf6f-105">Elle peut être envoyée à la routine de rappel seule ou combinée, à l’aide de l’opérateur OR, avec les notifications [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) et/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .</span><span class="sxs-lookup"><span data-stu-id="adf6f-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="adf6f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adf6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf6f-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="adf6f-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="adf6f-108">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations sur les chemins d’accès pour les fichiers source et cible.</span><span class="sxs-lookup"><span data-stu-id="adf6f-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="adf6f-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="adf6f-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="adf6f-110">Ce paramètre n’est pas utilisé, sauf si cette notification est combinée, à l’aide de l’opérateur OR, avec la notification [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) .</span><span class="sxs-lookup"><span data-stu-id="adf6f-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf6f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adf6f-111">Return value</span></span>

<span data-ttu-id="adf6f-112">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="adf6f-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="adf6f-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="adf6f-113">Return code</span></span>                                                                          | <span data-ttu-id="adf6f-114">Description</span><span class="sxs-lookup"><span data-stu-id="adf6f-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="adf6f-115"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="adf6f-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="adf6f-116">Remplacez le fichier dans le répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="adf6f-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="adf6f-117"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="adf6f-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="adf6f-118">Ignorer l’opération de copie en cours.</span><span class="sxs-lookup"><span data-stu-id="adf6f-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="adf6f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adf6f-119">Requirements</span></span>



| <span data-ttu-id="adf6f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adf6f-120">Requirement</span></span> | <span data-ttu-id="adf6f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf6f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adf6f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf6f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="adf6f-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adf6f-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="adf6f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf6f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="adf6f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adf6f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="adf6f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="adf6f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf6f-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf6f-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf6f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adf6f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf6f-129">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="adf6f-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="adf6f-130">Notifications</span><span class="sxs-lookup"><span data-stu-id="adf6f-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="adf6f-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="adf6f-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="adf6f-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="adf6f-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="adf6f-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="adf6f-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="adf6f-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="adf6f-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="adf6f-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="adf6f-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="adf6f-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="adf6f-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




