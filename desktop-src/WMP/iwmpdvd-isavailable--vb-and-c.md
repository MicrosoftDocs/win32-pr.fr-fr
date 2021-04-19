---
title: IWMPDVD. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- Lecteur Windows Media IWMPDVD. isAvailable (VB et C)
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531021"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="80bb6-104">IWMPDVD. isAvailable (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="80bb6-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="80bb6-105">La propriété **isAvailable** (la méthode **obtenir \_ isAvailable** en C#) obtient une valeur qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="80bb6-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="80bb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80bb6-106">Parameters</span></span>

<span data-ttu-id="80bb6-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="80bb6-107">*bstrItem*</span></span>

<span data-ttu-id="80bb6-108">System. String qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="80bb6-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="80bb6-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="80bb6-109">Value</span></span>      | <span data-ttu-id="80bb6-110">Description</span><span class="sxs-lookup"><span data-stu-id="80bb6-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bb6-111">Retour</span><span class="sxs-lookup"><span data-stu-id="80bb6-111">back</span></span>       | <span data-ttu-id="80bb6-112">Détecte si la méthode **IWMPDVD. Back** est disponible.</span><span class="sxs-lookup"><span data-stu-id="80bb6-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="80bb6-113">DVD</span><span class="sxs-lookup"><span data-stu-id="80bb6-113">dvd</span></span>        | <span data-ttu-id="80bb6-114">Détecte si le DVD est chargé.</span><span class="sxs-lookup"><span data-stu-id="80bb6-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="80bb6-115">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="80bb6-115">dvdDecoder</span></span> | <span data-ttu-id="80bb6-116">Détecte si le décodeur DVD est installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="80bb6-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="80bb6-117">resume</span><span class="sxs-lookup"><span data-stu-id="80bb6-117">resume</span></span>     | <span data-ttu-id="80bb6-118">Détecte si la méthode **IWMPDVD. Resume** est disponible.</span><span class="sxs-lookup"><span data-stu-id="80bb6-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="80bb6-119">titleMenu</span><span class="sxs-lookup"><span data-stu-id="80bb6-119">titleMenu</span></span>  | <span data-ttu-id="80bb6-120">Détecte si la méthode **IWMPDVD. titleMenu** est disponible.</span><span class="sxs-lookup"><span data-stu-id="80bb6-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="80bb6-121">Menu de la</span><span class="sxs-lookup"><span data-stu-id="80bb6-121">topMenu</span></span>    | <span data-ttu-id="80bb6-122">Détecte si la méthode de **menu IWMPDVD.** est disponible.</span><span class="sxs-lookup"><span data-stu-id="80bb6-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="80bb6-123">Communément appelé menu racine.</span><span class="sxs-lookup"><span data-stu-id="80bb6-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="80bb6-124">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="80bb6-124">Property Value</span></span>

<span data-ttu-id="80bb6-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="80bb6-125">**System.Boolean**</span></span>

<span data-ttu-id="80bb6-126">**System. Boolean** qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="80bb6-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="80bb6-127">Notes</span><span class="sxs-lookup"><span data-stu-id="80bb6-127">Remarks</span></span>

<span data-ttu-id="80bb6-128">Les fonctionnalités DVD du lecteur Windows Media ne fonctionneront pas sur les ordinateurs sur lesquels aucun décodeur de DVD n’est installé.</span><span class="sxs-lookup"><span data-stu-id="80bb6-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="80bb6-129">Vous pouvez déterminer si un décodeur est disponible en appelant la propriété **isAvailable** (la méthode « **obtenir \_ IsAvailable** » en C#) et en passant la valeur **System. String** « dvdDecoder ».</span><span class="sxs-lookup"><span data-stu-id="80bb6-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="80bb6-130">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="80bb6-130">Every DVD is authored differently.</span></span> <span data-ttu-id="80bb6-131">Les méthodes disponibles pendant la lecture et la navigation sur DVD dépendent de la façon dont le DVD est créé.</span><span class="sxs-lookup"><span data-stu-id="80bb6-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="80bb6-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80bb6-132">Requirements</span></span>



| <span data-ttu-id="80bb6-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80bb6-133">Requirement</span></span> | <span data-ttu-id="80bb6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="80bb6-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bb6-135">Version</span><span class="sxs-lookup"><span data-stu-id="80bb6-135">Version</span></span><br/>   | <span data-ttu-id="80bb6-136">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="80bb6-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="80bb6-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80bb6-137">Namespace</span></span><br/> | <span data-ttu-id="80bb6-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="80bb6-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="80bb6-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="80bb6-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="80bb6-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="80bb6-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80bb6-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80bb6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bb6-142">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="80bb6-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="80bb6-143">**IWMPDVD. Back (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="80bb6-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="80bb6-144">**IWMPDVD. Resume (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="80bb6-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="80bb6-145">**IWMPDVD. titleMenu (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="80bb6-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="80bb6-146">**Menu IWMPDVD. (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="80bb6-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





