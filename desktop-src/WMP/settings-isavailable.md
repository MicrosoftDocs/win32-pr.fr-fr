---
title: Settings. isAvailable
description: La propriété isAvailable indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. | Settings. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Paramètres. isAvailable du lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523583"
---
# <a name="settingsisavailable"></a><span data-ttu-id="3ac15-105">Settings. isAvailable</span><span class="sxs-lookup"><span data-stu-id="3ac15-105">Settings.isAvailable</span></span>

<span data-ttu-id="3ac15-106">La propriété **isAvailable** indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="3ac15-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac15-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ac15-107">Syntax</span></span>

<span data-ttu-id="3ac15-108">Player. Settings. isAvailable (Name)</span><span class="sxs-lookup"><span data-stu-id="3ac15-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="3ac15-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ac15-109">Parameters</span></span>

<span data-ttu-id="3ac15-110">*name*</span><span class="sxs-lookup"><span data-stu-id="3ac15-110">*name*</span></span>

<span data-ttu-id="3ac15-111">Chaîne contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ac15-111">String containing one of the following values.</span></span>



| <span data-ttu-id="3ac15-112">String</span><span class="sxs-lookup"><span data-stu-id="3ac15-112">String</span></span>             | <span data-ttu-id="3ac15-113">Description</span><span class="sxs-lookup"><span data-stu-id="3ac15-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="3ac15-114">démarrage automatique</span><span class="sxs-lookup"><span data-stu-id="3ac15-114">AutoStart</span></span>          | <span data-ttu-id="3ac15-115">Détermine si la propriété AutoStart peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="3ac15-116">Balance</span><span class="sxs-lookup"><span data-stu-id="3ac15-116">Balance</span></span>            | <span data-ttu-id="3ac15-117">Détermine si la propriété de solde peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="3ac15-118">BaseURL</span><span class="sxs-lookup"><span data-stu-id="3ac15-118">BaseURL</span></span>            | <span data-ttu-id="3ac15-119">Détermine si la propriété baseURL peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="3ac15-120">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="3ac15-120">DefaultFrame</span></span>       | <span data-ttu-id="3ac15-121">Détermine si la propriété defaultFrame peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="3ac15-122">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="3ac15-122">EnableErrorDialogs</span></span> | <span data-ttu-id="3ac15-123">Détermine si la propriété enableErrorDialogs peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="3ac15-124">GetMode</span><span class="sxs-lookup"><span data-stu-id="3ac15-124">GetMode</span></span>            | <span data-ttu-id="3ac15-125">Détermine si la méthode getMode peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="3ac15-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="3ac15-126">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="3ac15-126">InvokeURLs</span></span>         | <span data-ttu-id="3ac15-127">Détermine si la propriété invokeURLs peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="3ac15-128">Désactiver le son</span><span class="sxs-lookup"><span data-stu-id="3ac15-128">Mute</span></span>               | <span data-ttu-id="3ac15-129">Détermine si la propriété muet peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="3ac15-130">PlayCount</span><span class="sxs-lookup"><span data-stu-id="3ac15-130">PlayCount</span></span>          | <span data-ttu-id="3ac15-131">Détermine si la propriété playCount peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="3ac15-132">Tarif</span><span class="sxs-lookup"><span data-stu-id="3ac15-132">Rate</span></span>               | <span data-ttu-id="3ac15-133">Détermine si la propriété rate peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="3ac15-134">SetMode</span><span class="sxs-lookup"><span data-stu-id="3ac15-134">SetMode</span></span>            | <span data-ttu-id="3ac15-135">Détermine si la méthode setMode peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="3ac15-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="3ac15-136">Volume</span><span class="sxs-lookup"><span data-stu-id="3ac15-136">Volume</span></span>             | <span data-ttu-id="3ac15-137">Détermine si la propriété de volume peut être définie.</span><span class="sxs-lookup"><span data-stu-id="3ac15-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="3ac15-138">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3ac15-138">Return Values</span></span>

<span data-ttu-id="3ac15-139">Cette méthode retourne une valeur **booléenne** .</span><span class="sxs-lookup"><span data-stu-id="3ac15-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac15-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ac15-140">Requirements</span></span>



| <span data-ttu-id="3ac15-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ac15-141">Requirement</span></span> | <span data-ttu-id="3ac15-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ac15-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac15-143">Version</span><span class="sxs-lookup"><span data-stu-id="3ac15-143">Version</span></span><br/> | <span data-ttu-id="3ac15-144">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3ac15-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3ac15-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3ac15-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ac15-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ac15-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac15-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ac15-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac15-148">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="3ac15-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





