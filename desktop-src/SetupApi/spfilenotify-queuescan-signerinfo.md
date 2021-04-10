---
description: La \_ notification SPFILENOTIFY QUEUESCAN \_ signataires est envoyée à une routine de rappel par SetupScanFileQueue pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Message d’SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952360"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="cb110-103">\_Message SPFILENOTIFY QUEUESCAN \_ signataires</span><span class="sxs-lookup"><span data-stu-id="cb110-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="cb110-104">La notification **SPFILENOTIFY \_ QUEUESCAN \_ signataires** est envoyée à une routine de rappel par [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cb110-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="cb110-105">Cela se produit uniquement si la fonction **SetupScanFileQueue** a été appelée en spécifiant le rappel d’utilisation de l’indicateur SPQ \_ Scan \_ \_ \_ signataires.</span><span class="sxs-lookup"><span data-stu-id="cb110-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="cb110-106">Disponible à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb110-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="cb110-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb110-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb110-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="cb110-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="cb110-109">Pointeur vers une structure [**FILEPATHS \_ signataires**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) .</span><span class="sxs-lookup"><span data-stu-id="cb110-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="cb110-110">Le membre **cible** est le nom du fichier cible sur le système.</span><span class="sxs-lookup"><span data-stu-id="cb110-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="cb110-111">Le membre **source** est le chemin d’accès attendu du fichier source.</span><span class="sxs-lookup"><span data-stu-id="cb110-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="cb110-112">Le membre **Win32Error** est l’erreur de signature.</span><span class="sxs-lookup"><span data-stu-id="cb110-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="cb110-113">Les informations de signature sont retournées si la routine de rappel retourne **Win32Error**= = no \_ Error.</span><span class="sxs-lookup"><span data-stu-id="cb110-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="cb110-114">Le membre **DigitalSigner** est le signataire numérique.</span><span class="sxs-lookup"><span data-stu-id="cb110-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="cb110-115">Le membre **version** est la version.</span><span class="sxs-lookup"><span data-stu-id="cb110-115">The **Version** member is the version.</span></span> <span data-ttu-id="cb110-116">**CatalogFile** est le fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="cb110-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb110-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb110-117">Return value</span></span>

<span data-ttu-id="cb110-118">La routine de rappel doit retourner un [code d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cb110-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="cb110-119">Si la routine de rappel ne retourne aucune \_ erreur, l’analyse de la file d’attente continue et retourne si la routine retourne un autre code d’erreur, l’analyse de la file d’attente s’interrompt et [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retourne la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="cb110-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="cb110-120">Cette notification n’est pas gérée par la fonction [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="cb110-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb110-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb110-121">Requirements</span></span>



| <span data-ttu-id="cb110-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb110-122">Requirement</span></span> | <span data-ttu-id="cb110-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb110-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb110-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb110-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb110-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb110-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb110-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb110-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb110-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb110-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb110-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb110-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb110-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb110-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb110-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb110-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb110-131">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="cb110-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="cb110-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="cb110-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="cb110-133">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="cb110-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

