---
description: L’élément Group définit un groupe, l’objet de niveau supérieur dans une chronologie.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Group, élément (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950316"
---
# <a name="group-element"></a><span data-ttu-id="25eb0-103">Group, élément</span><span class="sxs-lookup"><span data-stu-id="25eb0-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="25eb0-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="25eb0-104">\[Deprecated.</span></span> <span data-ttu-id="25eb0-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25eb0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25eb0-106">L’élément **Group** définit un groupe, l’objet de niveau supérieur dans une chronologie.</span><span class="sxs-lookup"><span data-stu-id="25eb0-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="25eb0-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="25eb0-107">Attributes</span></span>

<span data-ttu-id="25eb0-108">[**bitdepth**](bitdepth-attribute.md), [**mise en mémoire tampon**](buffering-attribute.md), [**fréquence**](framerate-attribute.md)d’images, [**hauteur**](height-attribute.md), [**verrouillage**](lock-attribute.md), [**muet**](mute-attribute.md), [**nom**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nom d’utilisateur**](username-attribute.md), [**largeur**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="25eb0-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="25eb0-109">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="25eb0-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25eb0-110">Parent</span><span class="sxs-lookup"><span data-stu-id="25eb0-110">Parent</span></span>   | [<span data-ttu-id="25eb0-111">**actualité**</span><span class="sxs-lookup"><span data-stu-id="25eb0-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="25eb0-112">Children</span><span class="sxs-lookup"><span data-stu-id="25eb0-112">Children</span></span> | <span data-ttu-id="25eb0-113">[**composite**](composite-element.md), [**Effect**](effect-element.md), [**Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="25eb0-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="25eb0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="25eb0-114">Remarks</span></span>

<span data-ttu-id="25eb0-115">Dans un `group` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="25eb0-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="25eb0-116">La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.</span><span class="sxs-lookup"><span data-stu-id="25eb0-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="25eb0-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="25eb0-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="25eb0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25eb0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25eb0-119">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="25eb0-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



