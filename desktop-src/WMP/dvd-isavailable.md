---
title: DVD. isAvailable
description: La propriété isAvailable indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. | DVD. isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. isAvailable lecteur Windows Media
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522533"
---
# <a name="dvdisavailable"></a><span data-ttu-id="684e7-105">DVD. isAvailable</span><span class="sxs-lookup"><span data-stu-id="684e7-105">DVD.isAvailable</span></span>

<span data-ttu-id="684e7-106">La propriété **isAvailable** indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="684e7-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="684e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="684e7-107">Parameters</span></span>

<span data-ttu-id="684e7-108">*name*</span><span class="sxs-lookup"><span data-stu-id="684e7-108">*name*</span></span>

<span data-ttu-id="684e7-109">**Chaîne** contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="684e7-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="684e7-110">String</span><span class="sxs-lookup"><span data-stu-id="684e7-110">String</span></span>     | <span data-ttu-id="684e7-111">Description</span><span class="sxs-lookup"><span data-stu-id="684e7-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="684e7-112">Retour</span><span class="sxs-lookup"><span data-stu-id="684e7-112">back</span></span>       | <span data-ttu-id="684e7-113">Détermine si la méthode **Back** est disponible.</span><span class="sxs-lookup"><span data-stu-id="684e7-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="684e7-114">DVD</span><span class="sxs-lookup"><span data-stu-id="684e7-114">dvd</span></span>        | <span data-ttu-id="684e7-115">Détermine si le DVD est chargé.</span><span class="sxs-lookup"><span data-stu-id="684e7-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="684e7-116">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="684e7-116">dvdDecoder</span></span> | <span data-ttu-id="684e7-117">Détermine si le décodeur DVD est installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="684e7-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="684e7-118">resume</span><span class="sxs-lookup"><span data-stu-id="684e7-118">resume</span></span>     | <span data-ttu-id="684e7-119">Détermine si la méthode **Resume** est disponible.</span><span class="sxs-lookup"><span data-stu-id="684e7-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="684e7-120">titleMenu</span><span class="sxs-lookup"><span data-stu-id="684e7-120">titleMenu</span></span>  | <span data-ttu-id="684e7-121">Détermine si la méthode **titleMenu** est disponible.</span><span class="sxs-lookup"><span data-stu-id="684e7-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="684e7-122">Menu de la</span><span class="sxs-lookup"><span data-stu-id="684e7-122">topMenu</span></span>    | <span data-ttu-id="684e7-123">Détermine si la méthode de **menu** est disponible.</span><span class="sxs-lookup"><span data-stu-id="684e7-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="684e7-124">Communément appelé menu racine.</span><span class="sxs-lookup"><span data-stu-id="684e7-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="684e7-125">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="684e7-125">Return Values</span></span>

<span data-ttu-id="684e7-126">Cette méthode retourne une **valeur booléenne** en lecture seule qui indique si le paramètre spécifié est disponible.</span><span class="sxs-lookup"><span data-stu-id="684e7-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="684e7-127">Notes</span><span class="sxs-lookup"><span data-stu-id="684e7-127">Remarks</span></span>

<span data-ttu-id="684e7-128">Les fonctionnalités DVD du lecteur Windows Media ne fonctionneront pas sur les ordinateurs sur lesquels aucun décodeur de DVD tiers n’est installé.</span><span class="sxs-lookup"><span data-stu-id="684e7-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="684e7-129">Vous pouvez déterminer si un décodeur est disponible en appelant **isAvailable**(« dvdDecoder »).</span><span class="sxs-lookup"><span data-stu-id="684e7-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="684e7-130">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="684e7-130">Every DVD is authored differently.</span></span> <span data-ttu-id="684e7-131">Les méthodes disponibles pendant la lecture et la navigation sur DVD dépendent de la façon dont le DVD est créé.</span><span class="sxs-lookup"><span data-stu-id="684e7-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="684e7-132">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours **false**.</span><span class="sxs-lookup"><span data-stu-id="684e7-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="684e7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="684e7-133">Requirements</span></span>



| <span data-ttu-id="684e7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="684e7-134">Requirement</span></span> | <span data-ttu-id="684e7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="684e7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="684e7-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="684e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="684e7-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="684e7-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="684e7-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="684e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="684e7-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="684e7-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="684e7-140">Version</span><span class="sxs-lookup"><span data-stu-id="684e7-140">Version</span></span><br/>                  | <span data-ttu-id="684e7-141">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="684e7-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="684e7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="684e7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="684e7-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="684e7-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684e7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="684e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684e7-145">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="684e7-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





