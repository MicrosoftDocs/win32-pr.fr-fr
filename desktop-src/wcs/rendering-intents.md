---
title: Rendu des intentions
description: Le consortium de couleurs internationaux (ICC) a défini quatre valeurs différentes, appelées intentions de rendu.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS), rendu des intentions
- WCS (Windows Color System), rendu des intentions
- gestion des couleurs des images, rendu des intentions
- gestion des couleurs, rendu des intentions
- couleurs, rendu des intentions
- rendu des intentions
- ICC (International Color Consortium)
- IIC (International Color Consortium)
- Intention de l’image
- Intention graphique
- Intention de preuve
- Intention de correspondance
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523765"
---
# <a name="rendering-intents"></a><span data-ttu-id="a8328-115">Rendu des intentions</span><span class="sxs-lookup"><span data-stu-id="a8328-115">Rendering Intents</span></span>

<span data-ttu-id="a8328-116">Le consortium de couleurs internationaux (ICC) a défini quatre valeurs différentes, appelées *intentions de rendu*.</span><span class="sxs-lookup"><span data-stu-id="a8328-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="a8328-117">Elles représentent quatre approches différentes de la création d’un rendu des couleurs.</span><span class="sxs-lookup"><span data-stu-id="a8328-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="a8328-118">Ces quatre intentions, ainsi que les constantes utilisées pour y faire référence dans le code, sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8328-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="a8328-119">Intentionnel</span><span class="sxs-lookup"><span data-stu-id="a8328-119">Intent</span></span>                            | <span data-ttu-id="a8328-120">Nom ICC</span><span class="sxs-lookup"><span data-stu-id="a8328-120">ICC Name</span></span>              | <span data-ttu-id="a8328-121">Description</span><span class="sxs-lookup"><span data-stu-id="a8328-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="a8328-122">Image</span><span class="sxs-lookup"><span data-stu-id="a8328-122">Picture</span></span> | <span data-ttu-id="a8328-123">Perceptuelles</span><span class="sxs-lookup"><span data-stu-id="a8328-123">Perceptual</span></span>            | <span data-ttu-id="a8328-124">\_perception intentionnelle</span><span class="sxs-lookup"><span data-stu-id="a8328-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="a8328-125">Graphic</span><span class="sxs-lookup"><span data-stu-id="a8328-125">Graphic</span></span> | <span data-ttu-id="a8328-126">Saturation</span><span class="sxs-lookup"><span data-stu-id="a8328-126">Saturation</span></span>            | <span data-ttu-id="a8328-127">\_saturation intentionnelle</span><span class="sxs-lookup"><span data-stu-id="a8328-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="a8328-128">Proof</span><span class="sxs-lookup"><span data-stu-id="a8328-128">Proof</span></span>     | <span data-ttu-id="a8328-129">Colorimétrie relative</span><span class="sxs-lookup"><span data-stu-id="a8328-129">Relative Colorimetric</span></span> | <span data-ttu-id="a8328-130">\_Colorimétrie relative à l’intention \_</span><span class="sxs-lookup"><span data-stu-id="a8328-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="a8328-131">Correspond</span><span class="sxs-lookup"><span data-stu-id="a8328-131">Match</span></span>     | <span data-ttu-id="a8328-132">Colorimétrie absolue</span><span class="sxs-lookup"><span data-stu-id="a8328-132">Absolute Colorimetric</span></span> | <span data-ttu-id="a8328-133">\_Colorimétrie absolue \_ intentionnelle</span><span class="sxs-lookup"><span data-stu-id="a8328-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="a8328-134">La spécification de format de profil ICC version 3,4, qui décrit ces intentions, peut être téléchargée à partir de color.org.</span><span class="sxs-lookup"><span data-stu-id="a8328-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="a8328-135">Intention de l’image</span><span class="sxs-lookup"><span data-stu-id="a8328-135">Picture Intent</span></span>

<span data-ttu-id="a8328-136">Appelée « intention de perception » dans la clause de la spécification ICC 4,9, un motif d’image permet de compresser ou d’étendre la [gamme](./g.md) complète de l’image pour remplir la gamme de l’appareil de destination, de sorte que la balance grise soit préservée mais que la précision colorimétrique ne puisse pas être préservée.</span><span class="sxs-lookup"><span data-stu-id="a8328-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="a8328-137">En d’autres termes, si certaines couleurs d’une image se trouvent en dehors de la plage de couleurs que l’appareil de sortie peut afficher, l’intention de l’image est ajustée de façon à ce que toutes les couleurs de l’image se trouvent dans la plage qui peut être rendue et que la relation entre les couleurs soit conservée autant que possible.</span><span class="sxs-lookup"><span data-stu-id="a8328-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="a8328-138">Cet objectif est particulièrement adapté à l’affichage des photographies et des images, et est généralement l’intention par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8328-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="a8328-139">Intention graphique</span><span class="sxs-lookup"><span data-stu-id="a8328-139">Graphic Intent</span></span>

<span data-ttu-id="a8328-140">La clause de la spécification ICC 4,12 appelle l’intention graphique une intention de [saturation](s.md) .</span><span class="sxs-lookup"><span data-stu-id="a8328-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="a8328-141">Il conserve la chrominance des couleurs dans l’image au détriment de la [teinte](h.md) et de la [luminosité](l.md).</span><span class="sxs-lookup"><span data-stu-id="a8328-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="a8328-142">L’implémentation de cette intention reste un peu problématique, et la ICC continue de fonctionner sur les méthodes pour atteindre les effets souhaités.</span><span class="sxs-lookup"><span data-stu-id="a8328-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="a8328-143">Cet objectif est particulièrement adapté aux graphiques professionnels tels que les graphiques, où il est plus important que les couleurs soient éclatantes et contrastées les unes avec les autres plutôt qu’une couleur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a8328-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="a8328-144">Intention de preuve</span><span class="sxs-lookup"><span data-stu-id="a8328-144">Proof Intent</span></span>

<span data-ttu-id="a8328-145">L’intention de la preuve, appelée intention de colorimétrie dans la spécification ICC, est définie de telle sorte que toutes les couleurs qui se trouvent en dehors de la plage que le périphérique de sortie peut restituer soient ajustées à la couleur la plus proche qui peut être rendue, alors que toutes les autres couleurs restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="a8328-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="a8328-146">L’intention de la preuve ne préserve pas le [point blanc](w.md).</span><span class="sxs-lookup"><span data-stu-id="a8328-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="a8328-147">Par exemple, le blanc le plus blanc d’un papier est plus jaune que le blanc le plus blanc d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a8328-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="a8328-148">Une image convertie dans la gamme de l’imprimante à l’aide d’une intention de Colorimétrie relative entraînerait une plus grande couleur pour toutes les couleurs.</span><span class="sxs-lookup"><span data-stu-id="a8328-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="a8328-149">Le point blanc de l’image est déplacé pour correspondre au point blanc de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="a8328-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="a8328-150">Toutes les autres couleurs de l’image conservent leur position par rapport au point blanc.</span><span class="sxs-lookup"><span data-stu-id="a8328-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="a8328-151">Cela produit une image qui reflète de manière plus précise l’aspect de l’image imprimée.</span><span class="sxs-lookup"><span data-stu-id="a8328-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="a8328-152">Toutefois, l’utilisateur peut se déconcerter visuellement.</span><span class="sxs-lookup"><span data-stu-id="a8328-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="a8328-153">Intention de correspondance</span><span class="sxs-lookup"><span data-stu-id="a8328-153">Match Intent</span></span>

<span data-ttu-id="a8328-154">Dans un but de correspondance, toutes les couleurs qui se trouvent en dehors de la plage que le périphérique de sortie peut restituer sont ajustées à la couleur la plus proche qui peut être rendue, alors que toutes les autres couleurs restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="a8328-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="a8328-155">La spécification ICC appelle l’intention de l’intention de correspondance absolue colorimétrie.</span><span class="sxs-lookup"><span data-stu-id="a8328-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="a8328-156">L’intention de correspondance conserve le point blanc.</span><span class="sxs-lookup"><span data-stu-id="a8328-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="a8328-157">Par exemple, le blanc le plus blanc d’un papier est plus jaune que le blanc le plus blanc d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a8328-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="a8328-158">Une image convertie dans la [gamme](./g.md) de l’imprimante à l’aide de la fonction match a pour résultat que toutes les couleurs sont converties et mises en correspondance avec la gamme de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="a8328-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="a8328-159">Le point blanc de l’image n’est pas déplacé pour correspondre au point blanc de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="a8328-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="a8328-160">Par conséquent, la distance entre les couleurs et le point blanc peut changer.</span><span class="sxs-lookup"><span data-stu-id="a8328-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="a8328-161">Cela produit une image qui est moins visuellement déconcertée pour l’utilisateur, mais qui est également un rendu moins précis de la sortie de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="a8328-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 