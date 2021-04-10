---
description: La fonction PdhVbOpenQuery crée et Initialise une structure de requête unique qui est utilisée pour gérer la collection de données de performances.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115562"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="6e9c4-103">PdhVbOpenQuery fonction)</span><span class="sxs-lookup"><span data-stu-id="6e9c4-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="6e9c4-104">La fonction **PdhVbOpenQuery** crée et Initialise une structure de requête unique qui est utilisée pour gérer la collection de données de performances.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e9c4-105">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="6e9c4-106">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6e9c4-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="6e9c4-107">Function PdhVbOpenQuery ( \_ ByVal QueryHandle As long \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="6e9c4-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="6e9c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e9c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e9c4-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="6e9c4-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="6e9c4-110">Variable qui est désactivée (est égal à 0) avant l’appel de la fonction et, si la fonction réussit, contient l’ID unique de la requête créée et ouverte.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="6e9c4-111">Ce handle est utilisé dans les appels suivants à d’autres fonctions PDH pour identifier la requête.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e9c4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e9c4-112">Return value</span></span>

<span data-ttu-id="6e9c4-113">Si la fonction réussit, elle retourne un entier **long** égal à \_ l’erreur Success et un nouveau handle dans la variable *QueryHandle* .</span><span class="sxs-lookup"><span data-stu-id="6e9c4-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="6e9c4-114">Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6e9c4-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="6e9c4-115">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-115">The following are possible values.</span></span>



| <span data-ttu-id="6e9c4-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6e9c4-116">Return code</span></span>                                                                                                     | <span data-ttu-id="6e9c4-117">Description</span><span class="sxs-lookup"><span data-stu-id="6e9c4-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="6e9c4-118"><dt>**PDH \_ argument non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e9c4-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="6e9c4-119">L’argument n’est pas valide ou est incorrect.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="6e9c4-120"><dt>**\_échec d' \_ allocation de mémoire PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e9c4-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="6e9c4-121">Impossible d’allouer une mémoire tampon temporaire.</span><span class="sxs-lookup"><span data-stu-id="6e9c4-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e9c4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e9c4-122">Requirements</span></span>



| <span data-ttu-id="6e9c4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e9c4-123">Requirement</span></span> | <span data-ttu-id="6e9c4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e9c4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9c4-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9c4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9c4-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e9c4-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e9c4-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9c4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9c4-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e9c4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6e9c4-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e9c4-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e9c4-130"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e9c4-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e9c4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6e9c4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e9c4-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e9c4-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9c4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e9c4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9c4-134">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="6e9c4-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

