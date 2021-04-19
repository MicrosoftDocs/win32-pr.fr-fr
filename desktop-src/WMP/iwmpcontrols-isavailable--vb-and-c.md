---
title: IWMPControls. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur indiquant si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- Lecteur Windows Media IWMPControls. isAvailable (VB et C)
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537509"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="ef96f-104">IWMPControls. isAvailable (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="ef96f-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="ef96f-105">La propriété **isAvailable** (la méthode **obtenir \_ isAvailable** en C#) obtient une valeur indiquant si un type d’informations spécifié est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="ef96f-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="ef96f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef96f-106">Parameters</span></span>

<span data-ttu-id="ef96f-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="ef96f-107">*bstrItem*</span></span>

<span data-ttu-id="ef96f-108">System. String qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef96f-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="ef96f-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef96f-109">Value</span></span>           | <span data-ttu-id="ef96f-110">Description</span><span class="sxs-lookup"><span data-stu-id="ef96f-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef96f-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="ef96f-111">currentItem</span></span>     | <span data-ttu-id="ef96f-112">Découvre si l’utilisateur peut définir la propriété **IWMPControls. CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="ef96f-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="ef96f-113">currentMarker</span><span class="sxs-lookup"><span data-stu-id="ef96f-113">currentMarker</span></span>   | <span data-ttu-id="ef96f-114">Découvre si l’utilisateur peut effectuer une recherche sur un marqueur spécifique.</span><span class="sxs-lookup"><span data-stu-id="ef96f-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="ef96f-115">currentPosition</span><span class="sxs-lookup"><span data-stu-id="ef96f-115">currentPosition</span></span> | <span data-ttu-id="ef96f-116">Découvre si l’utilisateur peut rechercher une position spécifique dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ef96f-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="ef96f-117">Certains fichiers ne prennent pas en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="ef96f-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="ef96f-118">fastForward</span><span class="sxs-lookup"><span data-stu-id="ef96f-118">fastForward</span></span>     | <span data-ttu-id="ef96f-119">Détecte si le fichier prend en charge le transfert rapide et si cette fonctionnalité peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="ef96f-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="ef96f-120">De nombreux types de fichiers (et flux en direct) ne prennent pas en charge fastForward.</span><span class="sxs-lookup"><span data-stu-id="ef96f-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="ef96f-121">fastReverse</span><span class="sxs-lookup"><span data-stu-id="ef96f-121">fastReverse</span></span>     | <span data-ttu-id="ef96f-122">Détecte si le fichier prend en charge fastReverse et si cette fonctionnalité peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="ef96f-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="ef96f-123">De nombreux types de fichiers (et flux en direct) ne prennent pas en charge fastReverse.</span><span class="sxs-lookup"><span data-stu-id="ef96f-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="ef96f-124">Suivant</span><span class="sxs-lookup"><span data-stu-id="ef96f-124">next</span></span>            | <span data-ttu-id="ef96f-125">Détecte si l’utilisateur peut Rechercher l’entrée suivante dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="ef96f-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="ef96f-126">pause</span><span class="sxs-lookup"><span data-stu-id="ef96f-126">pause</span></span>           | <span data-ttu-id="ef96f-127">Détecte si la méthode **IWMPControls. pause** est disponible.</span><span class="sxs-lookup"><span data-stu-id="ef96f-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="ef96f-128">répétition</span><span class="sxs-lookup"><span data-stu-id="ef96f-128">play</span></span>            | <span data-ttu-id="ef96f-129">Détecte si la méthode **IWMPControls. Play** est disponible.</span><span class="sxs-lookup"><span data-stu-id="ef96f-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="ef96f-130">previous</span><span class="sxs-lookup"><span data-stu-id="ef96f-130">previous</span></span>        | <span data-ttu-id="ef96f-131">Détecte si l’utilisateur peut Rechercher l’entrée précédente dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="ef96f-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="ef96f-132">étape</span><span class="sxs-lookup"><span data-stu-id="ef96f-132">step</span></span>            | <span data-ttu-id="ef96f-133">Détecte si la méthode **IWMPControls2. Step** est disponible pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="ef96f-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="ef96f-134">stop</span><span class="sxs-lookup"><span data-stu-id="ef96f-134">stop</span></span>            | <span data-ttu-id="ef96f-135">Détecte si la méthode **IWMPControls. Stop** est disponible.</span><span class="sxs-lookup"><span data-stu-id="ef96f-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="ef96f-136">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="ef96f-136">Property Value</span></span>

<span data-ttu-id="ef96f-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="ef96f-137">**System.Boolean**</span></span>

<span data-ttu-id="ef96f-138">**System. Boolean** qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="ef96f-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef96f-139">Notes</span><span class="sxs-lookup"><span data-stu-id="ef96f-139">Remarks</span></span>

<span data-ttu-id="ef96f-140">**IWMPControls. isAvailable** est une propriété dans Visual Basic qui accepte un paramètre.</span><span class="sxs-lookup"><span data-stu-id="ef96f-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="ef96f-141">En C#, on parle de la méthode **IWMPControls. obten \_ isAvailable** .</span><span class="sxs-lookup"><span data-stu-id="ef96f-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="ef96f-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef96f-142">Examples</span></span>

<span data-ttu-id="ef96f-143">L’exemple suivant utilise la propriété **isAvailable** (méthode d’extraction de l’élément **\_ IsAvailable** en C#) pour vérifier que l’élément multimédia en cours prend en charge la propriété **CurrentPosition** .</span><span class="sxs-lookup"><span data-stu-id="ef96f-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="ef96f-144">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="ef96f-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="ef96f-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef96f-145">Requirements</span></span>



| <span data-ttu-id="ef96f-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef96f-146">Requirement</span></span> | <span data-ttu-id="ef96f-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef96f-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef96f-148">Version</span><span class="sxs-lookup"><span data-stu-id="ef96f-148">Version</span></span><br/>   | <span data-ttu-id="ef96f-149">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ef96f-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ef96f-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef96f-150">Namespace</span></span><br/> | <span data-ttu-id="ef96f-151">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ef96f-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ef96f-152">Assembly</span><span class="sxs-lookup"><span data-stu-id="ef96f-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ef96f-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ef96f-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef96f-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef96f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef96f-155">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef96f-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef96f-156">**IWMPControls. currentItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef96f-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef96f-157">**IWMPControls. pause (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef96f-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef96f-158">**IWMPControls. Play (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef96f-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef96f-159">**IWMPControls. Stop (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef96f-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef96f-160">**IWMPControls2. Step (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ef96f-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





