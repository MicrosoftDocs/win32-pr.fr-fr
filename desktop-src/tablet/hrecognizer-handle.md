---
description: Un descripteur HRECOGNIZER est utilisé pour créer un contexte de module de reconnaissance, récupérer les attributs et les propriétés du module de reconnaissance et déterminer les propriétés de paquet requises par le module de reconnaissance pour effectuer la reconnaissance.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Handle HRECOGNIZER (Récapitulatifis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318474"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="7daa0-103">Handle HRECOGNIZER</span><span class="sxs-lookup"><span data-stu-id="7daa0-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="7daa0-104">Un descripteur **HRECOGNIZER** est utilisé pour créer un contexte de module de reconnaissance, récupérer les attributs et les propriétés du module de reconnaissance et déterminer les propriétés de paquet requises par le module de reconnaissance pour effectuer la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="7daa0-105">Notes</span><span class="sxs-lookup"><span data-stu-id="7daa0-105">Remarks</span></span>

<span data-ttu-id="7daa0-106">Les fonctions suivantes utilisent un **HRECOGNIZER**.</span><span class="sxs-lookup"><span data-stu-id="7daa0-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="7daa0-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="7daa0-107">Function</span></span>                                                               | <span data-ttu-id="7daa0-108">Description</span><span class="sxs-lookup"><span data-stu-id="7daa0-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7daa0-109">**CreateRecognizer**</span><span class="sxs-lookup"><span data-stu-id="7daa0-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="7daa0-110">Crée un module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="7daa0-111">**DestroyRecognizer**</span><span class="sxs-lookup"><span data-stu-id="7daa0-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="7daa0-112">Détruit un module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="7daa0-113">**GetRecoAttributes**</span><span class="sxs-lookup"><span data-stu-id="7daa0-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="7daa0-114">Retourne les attributs du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="7daa0-115">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="7daa0-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="7daa0-116">Crée un contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="7daa0-117">**DestroyContext**</span><span class="sxs-lookup"><span data-stu-id="7daa0-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="7daa0-118">Détruit un contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="7daa0-119">**GetAllRecognizers**</span><span class="sxs-lookup"><span data-stu-id="7daa0-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="7daa0-120">Obtient tous les module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="7daa0-121">**GetResultPropertyList**</span><span class="sxs-lookup"><span data-stu-id="7daa0-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="7daa0-122">Récupère une liste de propriétés que le module de reconnaissance peut retourner pour une plage de résultats.</span><span class="sxs-lookup"><span data-stu-id="7daa0-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="7daa0-123">**GetPreferredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="7daa0-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="7daa0-124">Récupère une description de paquet qui contient les propriétés de paquet utilisées par le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="7daa0-125">**GetUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="7daa0-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="7daa0-126">Récupère les plages de points Unicode que le module de reconnaissance prend en charge.</span><span class="sxs-lookup"><span data-stu-id="7daa0-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="7daa0-127">**LoadCachedAttributes**</span><span class="sxs-lookup"><span data-stu-id="7daa0-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="7daa0-128">Charge les attributs mis en cache d’un module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7daa0-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="7daa0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7daa0-129">Requirements</span></span>



| <span data-ttu-id="7daa0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7daa0-130">Requirement</span></span> | <span data-ttu-id="7daa0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7daa0-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7daa0-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7daa0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7daa0-133">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7daa0-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="7daa0-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7daa0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7daa0-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7daa0-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="7daa0-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7daa0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7daa0-137"><dt>Récapitulatif</dt></span><span class="sxs-lookup"><span data-stu-id="7daa0-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




