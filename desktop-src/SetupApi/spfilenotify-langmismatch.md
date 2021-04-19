---
description: La \_ notification SPFILENOTIFY LANGMISMATCH est envoyée à la routine de rappel si la langue du fichier à copier ne correspond pas à la langue d’un fichier cible existant.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Message d’SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520763"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="3713b-103">\_Message SPFILENOTIFY LANGMISMATCH</span><span class="sxs-lookup"><span data-stu-id="3713b-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="3713b-104">La notification **SPFILENOTIFY \_ LANGMISMATCH** est envoyée à la routine de rappel si la langue du fichier à copier ne correspond pas à la langue d’un fichier cible existant.</span><span class="sxs-lookup"><span data-stu-id="3713b-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="3713b-105">Elle peut être envoyée à la routine de rappel seule ou combinée, à l’aide de l’opérateur OR, avec [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) et/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).</span><span class="sxs-lookup"><span data-stu-id="3713b-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="3713b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3713b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3713b-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="3713b-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="3713b-108">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations sur les chemins d’accès des fichiers source et cible.</span><span class="sxs-lookup"><span data-stu-id="3713b-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="3713b-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="3713b-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="3713b-110">Identifie les langages incompatibles.</span><span class="sxs-lookup"><span data-stu-id="3713b-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="3713b-111">Ce membre a l’identificateur de langue du fichier source dans le mot de poids faible et l’identificateur de langue du fichier cible existant dans le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="3713b-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3713b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3713b-112">Return value</span></span>

<span data-ttu-id="3713b-113">La routine de rappel doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3713b-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="3713b-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3713b-114">Return code</span></span>                                                                          | <span data-ttu-id="3713b-115">Description</span><span class="sxs-lookup"><span data-stu-id="3713b-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3713b-116"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="3713b-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="3713b-117">Copiez le fichier et remplacez le fichier existant.</span><span class="sxs-lookup"><span data-stu-id="3713b-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="3713b-118"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="3713b-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="3713b-119">Ignorez l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="3713b-119">Skip the copy operation.</span></span> <span data-ttu-id="3713b-120">Ne pas remplacer le fichier existant.</span><span class="sxs-lookup"><span data-stu-id="3713b-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3713b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3713b-121">Requirements</span></span>



| <span data-ttu-id="3713b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3713b-122">Requirement</span></span> | <span data-ttu-id="3713b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3713b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3713b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3713b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3713b-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3713b-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3713b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3713b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3713b-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3713b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3713b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3713b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3713b-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3713b-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3713b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3713b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3713b-131">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="3713b-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="3713b-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="3713b-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="3713b-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="3713b-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="3713b-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="3713b-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="3713b-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="3713b-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="3713b-136">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="3713b-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="3713b-137">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="3713b-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="3713b-138">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="3713b-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




