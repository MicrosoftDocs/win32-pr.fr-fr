---
description: L’ajout de brouillard à une scène 3D peut améliorer le réalisme, fournir des ambiance ou définir une humeur, et obscurcir les artefacts provoqués lorsque la géométrie à distance entre en vue.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514302"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="64612-103">Brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="64612-104">L’ajout de brouillard à une scène 3D peut améliorer le réalisme, fournir des ambiance ou définir une humeur, et obscurcir les artefacts provoqués lorsque la géométrie à distance entre en vue.</span><span class="sxs-lookup"><span data-stu-id="64612-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="64612-105">Direct3D prend en charge deux modèles de brouillard, le brouillard de pixel et le brouillard de vertex, chacun avec ses propres fonctionnalités et interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="64612-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="64612-106">Fondamentalement, le brouillard est implémenté en fusionnant la couleur des objets dans une scène avec une couleur de brouillard choisie en fonction de la profondeur d’un objet dans une scène ou de sa distance par rapport au point de vue.</span><span class="sxs-lookup"><span data-stu-id="64612-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="64612-107">À mesure que les objets sont plus éloignés, leur couleur d’origine fusionne de plus en plus avec la couleur de brouillard choisie, créant ainsi l’illusion que l’objet est de plus en plus obscurci par de petites particules flottantes dans la scène.</span><span class="sxs-lookup"><span data-stu-id="64612-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="64612-108">L’illustration suivante montre une scène rendue sans brouillard, et une scène similaire rendue avec Fog activé.</span><span class="sxs-lookup"><span data-stu-id="64612-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![illustration de la même scène avec et sans brouillard](images/fogcomp.png)

<span data-ttu-id="64612-110">Dans cette illustration, la scène sur la gauche présente un horizon clair, au-delà duquel aucun décor n’est visible, même s’il est visible dans le monde réel.</span><span class="sxs-lookup"><span data-stu-id="64612-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="64612-111">La scène sur la droite masque l’horizon en utilisant une couleur de brouillard identique à la couleur d’arrière-plan, ce qui fait apparaître les polygones dans la distance.</span><span class="sxs-lookup"><span data-stu-id="64612-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="64612-112">En associant des effets de brouillard discrets à la conception de scènes créatives, vous pouvez ajouter de l’humeur et adoucir la couleur des objets dans une scène.</span><span class="sxs-lookup"><span data-stu-id="64612-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="64612-113">Direct3D offre deux façons d’ajouter un brouillard à une scène : le brouillard de pixel et le brouillard de vertex, nommés pour la façon dont les effets de brouillard sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="64612-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="64612-114">Pour plus d’informations, consultez [brouillard de pixel (Direct3D 9)](pixel-fog.md) et [brouillard de vertex (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="64612-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="64612-115">En bref, le brouillard de pixel, également appelé « brouillard de table », est implémenté dans le pilote de périphérique et le brouillard de vertex est implémenté dans le moteur d’éclairage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="64612-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="64612-116">Une application peut implémenter un brouillard avec un nuanceur de sommets et un brouillard de pixel simultanément, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="64612-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="64612-117">Que vous utilisiez le brouillard de pixel ou de vertex, votre application doit fournir une matrice de projection conforme pour s’assurer que les effets de brouillard sont correctement appliqués.</span><span class="sxs-lookup"><span data-stu-id="64612-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="64612-118">Cette restriction s’applique même aux applications qui n’utilisent pas la transformation et le moteur d’éclairage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="64612-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="64612-119">Pour plus d’informations sur la façon dont vous pouvez fournir une matrice appropriée, consultez [projection Transform (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="64612-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="64612-120">Les rubriques suivantes présentent le brouillard et présentent des informations sur l’utilisation de diverses fonctionnalités de brouillard dans les applications Direct3D.</span><span class="sxs-lookup"><span data-stu-id="64612-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="64612-121">Formules de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="64612-122">Paramètres de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="64612-123">Fusion de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="64612-124">Couleur de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="64612-125">Brouillard du vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="64612-126">Brouillard de pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64612-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="64612-127">La fusion de brouillard est contrôlée par les États de rendu ; il ne fait pas partie du pipeline de pixels programmable.</span><span class="sxs-lookup"><span data-stu-id="64612-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64612-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64612-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64612-129">Rendu Direct3D</span><span class="sxs-lookup"><span data-stu-id="64612-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



