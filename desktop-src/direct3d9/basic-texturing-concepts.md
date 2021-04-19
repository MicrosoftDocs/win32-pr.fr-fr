---
description: Les premières images 3D générées par ordinateur, bien qu’elles soient généralement avancées pour leur temps, ont tendance à avoir un aspect plastique brillant.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Concepts de base de la texturation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513327"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="bf9c2-103">Concepts de base de la texturation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bf9c2-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="bf9c2-104">Les premières images 3D générées par ordinateur, bien qu’elles soient généralement avancées pour leur temps, ont tendance à avoir un aspect plastique brillant.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="bf9c2-105">Ils n’ont pas les mêmes types de marquages, tels que les scuffs, les fissures, les empreintes digitales et les taches, qui donnent aux objets 3D une complexité visuelle réaliste.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="bf9c2-106">Au cours des dernières années, les textures ont acquis la popularité des développeurs en tant qu’outil pour améliorer le réalisme des images 3D générées par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="bf9c2-107">Dans son utilisation quotidienne, la texture de mot fait référence à la régularité ou à l’irrégularité d’un objet.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="bf9c2-108">Toutefois, dans les graphiques informatiques, une texture est une image bitmap de couleurs de pixels qui donne à un objet l’apparence de la texture.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="bf9c2-109">Étant donné que les textures Direct3D sont des bitmaps, n’importe quelle bitmap peut être appliquée à une primitive Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="bf9c2-110">Par exemple, les applications peuvent créer et manipuler des objets qui semblent avoir un modèle de grain de bois.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="bf9c2-111">L’herbe, le saleté et les roches peuvent être appliqués à un ensemble de primitives 3D formant une colline.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="bf9c2-112">Le résultat est un Hillside réaliste.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="bf9c2-113">Vous pouvez également utiliser la texturation pour créer des effets tels que des signes sur une route, des strates de roches dans une falaise ou l’apparence d’un marbre sur un étage.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="bf9c2-114">En outre, Direct3D prend en charge des techniques de texturisation plus avancées, telles que la fusion de textures, avec ou sans transparence et un mappage de lumière.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="bf9c2-115">Pour plus d’informations, consultez [fusion de texture (Direct3D 9)](texture-blending.md) et [mappage de lumière avec des textures (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="bf9c2-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="bf9c2-116">Si votre application crée un périphérique de couche d’abstraction matérielle (HAL) ou un périphérique logiciel, il peut utiliser des textures 8, 16, 24, 32, 64 ou 128 bits.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="bf9c2-117">Des informations supplémentaires sont contenues dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf9c2-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="bf9c2-118">Modes d’adressage de la texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bf9c2-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="bf9c2-119">Régions de modification de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bf9c2-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="bf9c2-120">Palettes de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bf9c2-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="bf9c2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf9c2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9c2-122">Textures Direct3D</span><span class="sxs-lookup"><span data-stu-id="bf9c2-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



