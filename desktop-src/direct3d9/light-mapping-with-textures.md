---
description: Pour qu’une application affiche de manière réaliste une scène 3D, elle doit prendre en compte l’effet que les sources de lumière ont sur l’apparence de la scène.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Mise en correspondance de la lumière avec les textures (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513102"
---
# <a name="light-mapping-with-textures-direct3d-9"></a><span data-ttu-id="95ed3-103">Mise en correspondance de la lumière avec les textures (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="95ed3-103">Light Mapping with Textures (Direct3D 9)</span></span>

<span data-ttu-id="95ed3-104">Pour qu’une application affiche de manière réaliste une scène 3D, elle doit prendre en compte l’effet que les sources de lumière ont sur l’apparence de la scène.</span><span class="sxs-lookup"><span data-stu-id="95ed3-104">For an application to realistically render a 3D scene, it must take into account the effect that light sources have on the appearance of the scene.</span></span> <span data-ttu-id="95ed3-105">Bien que les techniques telles que l’ombrage plat et l’ombrage Gouraud soient des outils précieux à cet égard, elles peuvent être insuffisantes pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="95ed3-105">Although techniques such as flat and Gouraud shading are valuable tools in this respect, they can be insufficient for your needs.</span></span> <span data-ttu-id="95ed3-106">Direct3D prend en charge la fusion multipasse et plusieurs textures.</span><span class="sxs-lookup"><span data-stu-id="95ed3-106">Direct3D supports multipass and multiple texture blending.</span></span> <span data-ttu-id="95ed3-107">Ces fonctionnalités permettent à votre application de restituer des scènes avec une apparence plus réaliste que les scènes rendues uniquement avec des techniques d’ombrage.</span><span class="sxs-lookup"><span data-stu-id="95ed3-107">These capabilities enable your application to render scenes with a more realistic appearance than scenes rendered with shading techniques alone.</span></span> <span data-ttu-id="95ed3-108">En appliquant une ou plusieurs cartes de lumière, votre application peut mapper les zones de lumière et d’ombre sur ses Primitives.</span><span class="sxs-lookup"><span data-stu-id="95ed3-108">By applying one or more light maps, your application can map areas of light and shadow onto its primitives.</span></span>

<span data-ttu-id="95ed3-109">Une carte de lumière est une texture ou un groupe de textures qui contient des informations sur l’éclairage dans une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="95ed3-109">A light map is a texture or group of textures that contains information about lighting in a 3D scene.</span></span> <span data-ttu-id="95ed3-110">Vous pouvez stocker les informations d’éclairage dans les valeurs alpha de la carte de lumière, dans les valeurs de couleur, ou dans les deux.</span><span class="sxs-lookup"><span data-stu-id="95ed3-110">You can store the lighting information in the alpha values of the light map, in the color values, or in both.</span></span>

<span data-ttu-id="95ed3-111">Si vous implémentez le mappage de lumière à l’aide de la fusion de texture multipasse, votre application doit restituer la carte de lumière sur ses primitives au premier passage.</span><span class="sxs-lookup"><span data-stu-id="95ed3-111">If you implement light mapping using multipass texture blending, your application should render the light map onto its primitives on the first pass.</span></span> <span data-ttu-id="95ed3-112">Il doit utiliser une deuxième passe pour restituer la texture de base.</span><span class="sxs-lookup"><span data-stu-id="95ed3-112">It should use a second pass to render the base texture.</span></span> <span data-ttu-id="95ed3-113">La seule exception est le mappage de lumière spéculaire.</span><span class="sxs-lookup"><span data-stu-id="95ed3-113">The exception to this is specular light mapping.</span></span> <span data-ttu-id="95ed3-114">Dans ce cas, restituez d’abord la texture de base. Ajoutez ensuite la carte de lumière.</span><span class="sxs-lookup"><span data-stu-id="95ed3-114">In that case, render the base texture first; then add the light map.</span></span>

<span data-ttu-id="95ed3-115">La fusion de plusieurs textures permet à votre application de restituer la carte de lumière et la texture de base en une seule passe.</span><span class="sxs-lookup"><span data-stu-id="95ed3-115">Multiple texture blending enables your application to render the light map and the base texture in one pass.</span></span> <span data-ttu-id="95ed3-116">Si le matériel de l’utilisateur fournit une fusion multiple de texture, votre application doit en tirer parti lors de l’exécution du mappage de la lumière.</span><span class="sxs-lookup"><span data-stu-id="95ed3-116">If the user's hardware provides for multiple texture blending, your application should take advantage of it when performing light mapping.</span></span> <span data-ttu-id="95ed3-117">Cela améliore considérablement les performances de votre application.</span><span class="sxs-lookup"><span data-stu-id="95ed3-117">This significantly improves your application's performance.</span></span>

<span data-ttu-id="95ed3-118">Grâce aux cartes de lumière, une application Direct3D peut obtenir un large éventail d’effets d’éclairage lors du rendu de Primitives.</span><span class="sxs-lookup"><span data-stu-id="95ed3-118">Using light maps, a Direct3D application can achieve a variety of lighting effects when it renders primitives.</span></span> <span data-ttu-id="95ed3-119">Il peut également mapper des lumières monochromes et colorées dans une scène, mais il peut également ajouter des détails tels que des surbrillances spéculaires et un éclairage diffus.</span><span class="sxs-lookup"><span data-stu-id="95ed3-119">It can map not only monochrome and colored lights in a scene, but it can also add details such as specular highlights and diffuse lighting.</span></span>

<span data-ttu-id="95ed3-120">Des informations sur l’utilisation de la fusion de texture Direct3D pour effectuer un mappage de lumière sont présentées dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="95ed3-120">Information on using Direct3D texture blending to perform light mapping is presented in the following topics.</span></span>

-   [<span data-ttu-id="95ed3-121">Cartes de lumière monochromes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="95ed3-121">Monochrome Light Maps (Direct3D 9)</span></span>](monochrome-light-maps.md)
-   [<span data-ttu-id="95ed3-122">Cartes de lumière de couleur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="95ed3-122">Color Light Maps (Direct3D 9)</span></span>](color-light-maps.md)
-   [<span data-ttu-id="95ed3-123">Cartes de lumière spéculaire (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="95ed3-123">Specular Light Maps (Direct3D 9)</span></span>](specular-light-maps.md)
-   [<span data-ttu-id="95ed3-124">Cartes de lumière diffuse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="95ed3-124">Diffuse Light Maps (Direct3D 9)</span></span>](diffuse-light-maps.md)

## <a name="related-topics"></a><span data-ttu-id="95ed3-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95ed3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95ed3-126">Fusion de texture</span><span class="sxs-lookup"><span data-stu-id="95ed3-126">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 



