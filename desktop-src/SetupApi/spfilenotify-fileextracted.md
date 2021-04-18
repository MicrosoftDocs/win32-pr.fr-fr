---
description: La \_ notification SPFILENOTIFY FILEEXTRACTED est envoyée à une routine de rappel par SetupIterateCabinet pour indiquer qu’un fichier a été extrait du fichier CAB ou qu’une extraction a échoué et que le traitement de l’armoire a été annulé.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Message d’SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519548"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="0ebd9-103">\_Message SPFILENOTIFY FILEEXTRACTED</span><span class="sxs-lookup"><span data-stu-id="0ebd9-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="0ebd9-104">La notification **SPFILENOTIFY \_ FILEEXTRACTED** est envoyée à une routine de rappel par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour indiquer qu’un fichier a été extrait du fichier CAB ou qu’une extraction a échoué et que le traitement de l’armoire a été annulé.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="0ebd9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ebd9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebd9-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="0ebd9-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebd9-107">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations de chemin d’accès pour le fichier extrait.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="0ebd9-108">Le membre **sourceFile** de la structure **FILEPATHS** contient le chemin d’accès source complet du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="0ebd9-109">Le membre **TargetFile** fournit le chemin d’accès cible complet du fichier à installer sur le système.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0ebd9-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0ebd9-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebd9-111">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebd9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ebd9-112">Return value</span></span>

<span data-ttu-id="0ebd9-113">La routine de rappel du fichier cab doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="0ebd9-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0ebd9-114">Return code</span></span>                                                                               | <span data-ttu-id="0ebd9-115">Description</span><span class="sxs-lookup"><span data-stu-id="0ebd9-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ebd9-116"><dt>**AUCUNE \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd9-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="0ebd9-117">Aucune erreur ne s’est produite. poursuivez le traitement du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="0ebd9-118"><dt>**ERREUR \_ xxx**</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd9-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="0ebd9-119">Une erreur du type spécifié s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-119">An error of the specified type occurred.</span></span> <span data-ttu-id="0ebd9-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="0ebd9-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="0ebd9-122">Aucune routine de rappel d’armoire par défaut n’est fournie avec l’API d’installation.</span><span class="sxs-lookup"><span data-stu-id="0ebd9-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="0ebd9-123">Votre application de configuration doit fournir une routine de rappel pour gérer les notifications envoyées par la fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="0ebd9-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ebd9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ebd9-124">Requirements</span></span>



| <span data-ttu-id="0ebd9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ebd9-125">Requirement</span></span> | <span data-ttu-id="0ebd9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ebd9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebd9-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ebd9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebd9-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ebd9-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0ebd9-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ebd9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebd9-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ebd9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ebd9-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ebd9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebd9-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd9-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebd9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ebd9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebd9-134">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="0ebd9-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0ebd9-135">Notifications</span><span class="sxs-lookup"><span data-stu-id="0ebd9-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0ebd9-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="0ebd9-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="0ebd9-137">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="0ebd9-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

