---
description: L’élément Group définit un groupe, l’objet de niveau supérieur dans une chronologie.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Group, élément (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909247"
---
# <a name="group-element"></a><span data-ttu-id="fce03-103">Group, élément</span><span class="sxs-lookup"><span data-stu-id="fce03-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="fce03-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fce03-104">\[Deprecated.</span></span> <span data-ttu-id="fce03-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fce03-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fce03-106">L’élément **Group** définit un groupe, l’objet de niveau supérieur dans une chronologie.</span><span class="sxs-lookup"><span data-stu-id="fce03-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="fce03-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="fce03-107">Attributes</span></span>

<span data-ttu-id="fce03-108">[**bitdepth**](bitdepth-attribute.md), [**mise en mémoire tampon**](buffering-attribute.md), [**fréquence**](framerate-attribute.md)d’images, [**hauteur**](height-attribute.md), [**verrouillage**](lock-attribute.md), [**muet**](mute-attribute.md), [**nom**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nom d’utilisateur**](username-attribute.md), [**largeur**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="fce03-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="fce03-109">Informations parent/enfant</span><span class="sxs-lookup"><span data-stu-id="fce03-109">Parent/Child Information</span></span>



| <span data-ttu-id="fce03-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="fce03-110">Label</span></span> | <span data-ttu-id="fce03-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fce03-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce03-112">Parent</span><span class="sxs-lookup"><span data-stu-id="fce03-112">Parent</span></span>   | [<span data-ttu-id="fce03-113">**actualité**</span><span class="sxs-lookup"><span data-stu-id="fce03-113">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="fce03-114">Children</span><span class="sxs-lookup"><span data-stu-id="fce03-114">Children</span></span> | <span data-ttu-id="fce03-115">[**composite**](composite-element.md), [**Effect**](effect-element.md), [**Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="fce03-115">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fce03-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fce03-116">Remarks</span></span>

<span data-ttu-id="fce03-117">Dans un `group` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="fce03-117">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="fce03-118">La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.</span><span class="sxs-lookup"><span data-stu-id="fce03-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="fce03-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="fce03-119">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="fce03-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce03-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce03-121">Éléments XTL</span><span class="sxs-lookup"><span data-stu-id="fce03-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



