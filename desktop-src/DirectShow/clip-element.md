---
description: Le clip epecifies une source de média.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Élément clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908667"
---
# <a name="clip-element"></a><span data-ttu-id="c8985-103">Élément clip</span><span class="sxs-lookup"><span data-stu-id="c8985-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="c8985-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c8985-104">\[Deprecated.</span></span> <span data-ttu-id="c8985-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8985-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c8985-106">`clip`Epecifies une source de média.</span><span class="sxs-lookup"><span data-stu-id="c8985-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="c8985-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="c8985-107">Attributes</span></span>

<span data-ttu-id="c8985-108">[**CLSID**](clsid-attribute.md), [**cadence**](framerate-attribute.md), [**Lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**muet**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="c8985-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="c8985-109">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="c8985-109">Parent/Child Information</span></span>



| <span data-ttu-id="c8985-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="c8985-110">Label</span></span> | <span data-ttu-id="c8985-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8985-111">Value</span></span> |
|----------|----------------------------------|
| <span data-ttu-id="c8985-112">Parent</span><span class="sxs-lookup"><span data-stu-id="c8985-112">Parent</span></span>   | [<span data-ttu-id="c8985-113">**track**</span><span class="sxs-lookup"><span data-stu-id="c8985-113">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="c8985-114">Children</span><span class="sxs-lookup"><span data-stu-id="c8985-114">Children</span></span> | [<span data-ttu-id="c8985-115">**résultat**</span><span class="sxs-lookup"><span data-stu-id="c8985-115">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="c8985-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8985-116">Remarks</span></span>

<span data-ttu-id="c8985-117">L’attribut **CLSID** spécifie le CLSID d’un filtre source à utiliser comme source.</span><span class="sxs-lookup"><span data-stu-id="c8985-117">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="c8985-118">Ne spécifiez pas les attributs **src** et **CLSID** dans le même `clip` élément.</span><span class="sxs-lookup"><span data-stu-id="c8985-118">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="c8985-119">Spécifiez au moins un attribut Start-Time (**Start** ou **mstart**) et un attribut Stop-Time (**Stop** ou **mstop**).</span><span class="sxs-lookup"><span data-stu-id="c8985-119">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="c8985-120">Si l’un des attributs de démarrage n’est pas spécifié, la valeur par défaut est 0 (le début de la chronologie pour **Start** ou le début de la séquence pour **mstart**).</span><span class="sxs-lookup"><span data-stu-id="c8985-120">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="c8985-121">Si l’un des attributs d’arrêt n’est pas spécifié, l’algorithme DES prend une vitesse de lecture normale et calcule l’heure d’arrêt non spécifiée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c8985-121">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="c8985-122">Si les deux temps d’arrêt sont spécifiés, la lecture est plus rapide ou plus lente que la normale, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c8985-122">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="c8985-123">Dans l’exemple suivant, la durée de la chronologie est de sept secondes (**Stop** moins **Start**).</span><span class="sxs-lookup"><span data-stu-id="c8985-123">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="c8985-124">La vitesse de lecture normale est supposée. par conséquent, l’heure d’arrêt du support est par défaut de 10 secondes (durée plus **mstart**).</span><span class="sxs-lookup"><span data-stu-id="c8985-124">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="c8985-125">Dans l’exemple suivant, l’heure de début du média est définie par défaut sur 0, ce qui force la durée du support à être de 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="c8985-125">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="c8985-126">La durée de la chronologie est de cinq secondes, de sorte que le clip est lu à deux fois la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="c8985-126">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="c8985-127">Si l’attribut **src** spécifie une image continue, des tentatives de chargement d’une série d’images fixes pour créer une animation.</span><span class="sxs-lookup"><span data-stu-id="c8985-127">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="c8985-128">Par exemple, si l’attribut **src** est IMAGE001.BMP, le recherche des IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, etc.</span><span class="sxs-lookup"><span data-stu-id="c8985-128">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="c8985-129">En supposant qu’elles existent, elles sont affichées dans l’ordre numérique séquentiel, à la vitesse spécifiée par l’attribut **cadence** .</span><span class="sxs-lookup"><span data-stu-id="c8985-129">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="c8985-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="c8985-130">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="c8985-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8985-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8985-132">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="c8985-132">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



