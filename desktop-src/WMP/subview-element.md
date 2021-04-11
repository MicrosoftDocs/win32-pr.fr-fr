---
title: Subview, élément
description: Subview, élément
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Apparences du lecteur Windows Media, élément de sous-affichage
- Skins, subview, élément
- Subview, élément
- référence pour les apparences, élément de sous-affichage
- éléments, sous-affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310970"
---
# <a name="subview-element"></a><span data-ttu-id="565cf-108">Subview, élément</span><span class="sxs-lookup"><span data-stu-id="565cf-108">SUBVIEW Element</span></span>

<span data-ttu-id="565cf-109">L’élément de sous- **affichage** permet de manipuler une partie d’une apparence, par exemple pour fournir un panneau de configuration qui peut être masqué lorsqu’il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="565cf-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="565cf-110">Les éléments de la sous- **vue** sont toujours des enfants des éléments d' **affichage** parents et peuvent contenir d’autres éléments d’apparence, à l’exception de la **vue**, du **thème** et d’autres éléments de la sous- **vue** .</span><span class="sxs-lookup"><span data-stu-id="565cf-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="565cf-111">L’élément **subview** prend en charge les attributs suivants, qui sont définis sous l’élément **View** .</span><span class="sxs-lookup"><span data-stu-id="565cf-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="565cf-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="565cf-112">Attribute</span></span>                                                       | <span data-ttu-id="565cf-113">Description</span><span class="sxs-lookup"><span data-stu-id="565cf-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="565cf-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="565cf-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="565cf-115">Spécifie ou récupère la couleur d’arrière-plan du contrôle de sous- **affichage** .</span><span class="sxs-lookup"><span data-stu-id="565cf-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="565cf-116">La valeur par défaut est « None ».</span><span class="sxs-lookup"><span data-stu-id="565cf-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="565cf-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="565cf-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="565cf-118">Spécifie ou récupère l’image d’arrière-plan du contrôle de sous- **affichage** .</span><span class="sxs-lookup"><span data-stu-id="565cf-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="565cf-119">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="565cf-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="565cf-120">Spécifie ou récupère la valeur de décalage de la teinte de l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="565cf-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="565cf-121">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="565cf-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="565cf-122">Spécifie ou récupère la valeur de saturation de l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="565cf-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="565cf-123">backgroundTiled</span><span class="sxs-lookup"><span data-stu-id="565cf-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="565cf-124">Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan du contrôle de sous- **affichage** est affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="565cf-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="565cf-125">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="565cf-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="565cf-126">Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="565cf-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="565cf-127">Transparente</span><span class="sxs-lookup"><span data-stu-id="565cf-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="565cf-128">Spécifie ou récupère la couleur de transparence de l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="565cf-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="565cf-129">L’élément **subview** prend en charge les attributs ambiants, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="565cf-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="565cf-130">Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="565cf-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="565cf-131">L’élément **subview** peut implémenter les gestionnaires d’événements ambiants suivants : [onendmove](onendmove.md) et [OnResize](onresize.md).</span><span class="sxs-lookup"><span data-stu-id="565cf-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="565cf-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="565cf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="565cf-133">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="565cf-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="565cf-134">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="565cf-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 




