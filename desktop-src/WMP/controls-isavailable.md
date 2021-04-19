---
title: Controls. isAvailable
description: La propriété isAvailable indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. | Controls. isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controls. isAvailable lecteur Windows Media
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539951"
---
# <a name="controlsisavailable"></a><span data-ttu-id="a3306-105">Controls. isAvailable</span><span class="sxs-lookup"><span data-stu-id="a3306-105">Controls.isAvailable</span></span>

<span data-ttu-id="a3306-106">La propriété **isAvailable** indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="a3306-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="a3306-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3306-107">Parameters</span></span>

<span data-ttu-id="a3306-108">*name*</span><span class="sxs-lookup"><span data-stu-id="a3306-108">*name*</span></span>

<span data-ttu-id="a3306-109">**Chaîne** contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3306-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="a3306-110">String</span><span class="sxs-lookup"><span data-stu-id="a3306-110">String</span></span>          | <span data-ttu-id="a3306-111">Description</span><span class="sxs-lookup"><span data-stu-id="a3306-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3306-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="a3306-112">currentItem</span></span>     | <span data-ttu-id="a3306-113">Détermine si l’utilisateur peut définir la propriété **CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="a3306-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="a3306-114">currentMarker</span><span class="sxs-lookup"><span data-stu-id="a3306-114">currentMarker</span></span>   | <span data-ttu-id="a3306-115">Détermine si l’utilisateur peut effectuer une recherche sur un marqueur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a3306-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="a3306-116">currentPosition</span><span class="sxs-lookup"><span data-stu-id="a3306-116">currentPosition</span></span> | <span data-ttu-id="a3306-117">Détermine si l’utilisateur peut rechercher une position spécifique dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="a3306-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="a3306-118">Certains fichiers ne prennent pas en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="a3306-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="a3306-119">fastForward</span><span class="sxs-lookup"><span data-stu-id="a3306-119">fastForward</span></span>     | <span data-ttu-id="a3306-120">Détermine si le fichier prend en charge le transfert rapide et si cette fonctionnalité peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="a3306-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="a3306-121">De nombreux types de fichiers (ou flux en direct) ne prennent pas en charge fastForward.</span><span class="sxs-lookup"><span data-stu-id="a3306-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="a3306-122">fastReverse</span><span class="sxs-lookup"><span data-stu-id="a3306-122">fastReverse</span></span>     | <span data-ttu-id="a3306-123">Détermine si le fichier prend en charge fastReverse et si cette fonctionnalité peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="a3306-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="a3306-124">De nombreux types de fichiers (ou flux en direct) ne prennent pas en charge fastReverse.</span><span class="sxs-lookup"><span data-stu-id="a3306-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="a3306-125">Suivant</span><span class="sxs-lookup"><span data-stu-id="a3306-125">next</span></span>            | <span data-ttu-id="a3306-126">Détermine si l’utilisateur peut Rechercher l’entrée suivante dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="a3306-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="a3306-127">pause</span><span class="sxs-lookup"><span data-stu-id="a3306-127">pause</span></span>           | <span data-ttu-id="a3306-128">Détermine si la méthode **Pause** est disponible.</span><span class="sxs-lookup"><span data-stu-id="a3306-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="a3306-129">répétition</span><span class="sxs-lookup"><span data-stu-id="a3306-129">play</span></span>            | <span data-ttu-id="a3306-130">Détermine si la méthode de **lecture** est disponible.</span><span class="sxs-lookup"><span data-stu-id="a3306-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="a3306-131">previous</span><span class="sxs-lookup"><span data-stu-id="a3306-131">previous</span></span>        | <span data-ttu-id="a3306-132">Détermine si l’utilisateur peut Rechercher l’entrée précédente dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="a3306-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="a3306-133">étape</span><span class="sxs-lookup"><span data-stu-id="a3306-133">step</span></span>            | <span data-ttu-id="a3306-134">Détermine si la méthode **Step** est disponible pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="a3306-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="a3306-135">stop</span><span class="sxs-lookup"><span data-stu-id="a3306-135">stop</span></span>            | <span data-ttu-id="a3306-136">Détermine si la méthode **Stop** est disponible.</span><span class="sxs-lookup"><span data-stu-id="a3306-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="a3306-137">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a3306-137">Return Values</span></span>

<span data-ttu-id="a3306-138">Cette méthode retourne une valeur **booléenne** .</span><span class="sxs-lookup"><span data-stu-id="a3306-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="a3306-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="a3306-139">Examples</span></span>

<span data-ttu-id="a3306-140">L’exemple suivant crée un élément bouton HTML qui cherche à la position de départ de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="a3306-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="a3306-141">Le code JScript utilise **isAvailable** pour vérifier que le fichier prend en charge l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="a3306-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="a3306-142">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a3306-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="a3306-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3306-143">Requirements</span></span>



| <span data-ttu-id="a3306-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3306-144">Requirement</span></span> | <span data-ttu-id="a3306-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3306-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3306-146">Version</span><span class="sxs-lookup"><span data-stu-id="a3306-146">Version</span></span><br/> | <span data-ttu-id="a3306-147">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3306-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="a3306-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a3306-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3306-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3306-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3306-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3306-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3306-151">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="a3306-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





