---
description: La \_ notification SPFILENOTIFY FILEINCABINET est envoyée à une routine de rappel par SetupIterateCabinet pour chaque fichier trouvé dans le fichier CAB. La routine de rappel doit retourner une valeur indiquant s’il faut extraire le fichier.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Message d’SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526301"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="8d26e-104">\_Message SPFILENOTIFY FILEINCABINET</span><span class="sxs-lookup"><span data-stu-id="8d26e-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="8d26e-105">La notification **SPFILENOTIFY \_ FILEINCABINET** est envoyée à une routine de rappel par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour chaque fichier trouvé dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="8d26e-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="8d26e-106">La routine de rappel doit retourner une valeur indiquant s’il faut extraire le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d26e-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="8d26e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d26e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d26e-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="8d26e-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="8d26e-109">Pointeur vers un [**fichier dans la structure d' \_ \_ \_ informations**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) du fichier CAB qui contient des informations sur le fichier dans le cabinet.</span><span class="sxs-lookup"><span data-stu-id="8d26e-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="8d26e-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="8d26e-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="8d26e-111">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de fichier du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="8d26e-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d26e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d26e-112">Return value</span></span>

<span data-ttu-id="8d26e-113">Votre routine de rappel doit retourner l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8d26e-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="8d26e-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8d26e-114">Return code</span></span>                                                                                 | <span data-ttu-id="8d26e-115">Description</span><span class="sxs-lookup"><span data-stu-id="8d26e-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8d26e-116"><dt>**FILEOP \_ Ignorer**</dt></span><span class="sxs-lookup"><span data-stu-id="8d26e-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="8d26e-117">N’extrayez pas le fichier, ignorez-le.</span><span class="sxs-lookup"><span data-stu-id="8d26e-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="8d26e-118"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="8d26e-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="8d26e-119">Extrayez le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d26e-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="8d26e-120">Si votre routine de rappel retourne FILEOP \_ doit, le nom à utiliser pour le fichier extrait doit être spécifié dans le membre **FullTargetName** du [**fichier dans la structure d' \_ \_ \_ informations du fichier CAB**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) passé à la routine dans *param1*.</span><span class="sxs-lookup"><span data-stu-id="8d26e-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="8d26e-121">Il n’existe aucune routine de rappel d’armoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="8d26e-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="8d26e-122">L’application d’installation doit fournir une routine de rappel pour gérer les notifications envoyées par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="8d26e-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d26e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d26e-123">Requirements</span></span>



| <span data-ttu-id="8d26e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d26e-124">Requirement</span></span> | <span data-ttu-id="8d26e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d26e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d26e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d26e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8d26e-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d26e-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8d26e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d26e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8d26e-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d26e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d26e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d26e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d26e-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d26e-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d26e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d26e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d26e-133">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="8d26e-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="8d26e-134">Notifications</span><span class="sxs-lookup"><span data-stu-id="8d26e-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="8d26e-135">**fichier \_ dans le fichier \_ CAB \_**</span><span class="sxs-lookup"><span data-stu-id="8d26e-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="8d26e-136">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="8d26e-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




