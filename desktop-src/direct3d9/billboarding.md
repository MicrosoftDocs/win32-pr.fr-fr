---
description: Lorsque vous créez des scènes 3D, une application peut parfois obtenir des avantages en matière de performances en affichant des objets 2D de manière à ce qu’ils apparaissent comme des objets 3D. Il s’agit de l’idée de base qui sous-tend la technique d’un billboarding.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Billboarding (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519233"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="58e09-104">Billboarding (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="58e09-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="58e09-105">Lorsque vous créez des scènes 3D, une application peut parfois obtenir des avantages en matière de performances en affichant des objets 2D de manière à ce qu’ils apparaissent comme des objets 3D.</span><span class="sxs-lookup"><span data-stu-id="58e09-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="58e09-106">Il s’agit de l’idée de base qui sous-tend la technique d’un billboarding.</span><span class="sxs-lookup"><span data-stu-id="58e09-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="58e09-107">Un tableau blanc dans le sens normal du mot est un signe sur une route.</span><span class="sxs-lookup"><span data-stu-id="58e09-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="58e09-108">Les applications Microsoft Direct3D peuvent créer et afficher ce type de panneaux en définissant un solide rectangulaire et en lui appliquant une texture.</span><span class="sxs-lookup"><span data-stu-id="58e09-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="58e09-109">L’affichage des panneaux dans le sens le plus spécialisé des graphiques 3D est une extension de ce.</span><span class="sxs-lookup"><span data-stu-id="58e09-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="58e09-110">L’objectif est de faire en sorte que les objets 2D apparaissent en 3D.</span><span class="sxs-lookup"><span data-stu-id="58e09-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="58e09-111">La technique consiste à appliquer une texture qui contient l’image de l’objet à une primitive rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="58e09-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="58e09-112">La primitive est pivotée afin d’être toujours face à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58e09-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="58e09-113">Peu importe si l’image de l’objet n’est pas rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="58e09-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="58e09-114">Les parties du panneau peuvent être rendues transparentes, donc les parties de l’image de tableau que vous ne souhaitez pas voir ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="58e09-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="58e09-115">De nombreux jeux utilisent le billboarding pour les sprites animés.</span><span class="sxs-lookup"><span data-stu-id="58e09-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="58e09-116">Par exemple, lorsque l’utilisateur parcourt un labyrinthe 3D, il peut voir des armes ou des récompenses qui peuvent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="58e09-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="58e09-117">Il s’agit généralement d’images 2D texturées sur une primitive rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="58e09-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="58e09-118">Le billboarding est souvent utilisé dans les jeux pour restituer des images d’arbres, d’arbustes et de clouds.</span><span class="sxs-lookup"><span data-stu-id="58e09-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="58e09-119">Quand une image est appliquée à un panneau, la primitive rectangulaire doit d’abord être pivotée afin que l’image résultante fasse face à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58e09-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="58e09-120">Votre application doit ensuite la traduire en position.</span><span class="sxs-lookup"><span data-stu-id="58e09-120">Your application must then translate it into position.</span></span> <span data-ttu-id="58e09-121">L’application peut ensuite appliquer une texture à la primitive.</span><span class="sxs-lookup"><span data-stu-id="58e09-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="58e09-122">Le billboarding fonctionne mieux pour les objets symétriques, en particulier les objets qui sont symétriques le long de l’axe vertical.</span><span class="sxs-lookup"><span data-stu-id="58e09-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="58e09-123">Elle requiert également que l’altitude du point de vue n’augmente pas trop.</span><span class="sxs-lookup"><span data-stu-id="58e09-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="58e09-124">Si l’utilisateur est autorisé à afficher le panneau d’affichage ci-dessus, il devient évident que l’objet est 2D plutôt que 3D.</span><span class="sxs-lookup"><span data-stu-id="58e09-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58e09-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58e09-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e09-126">Exemples alpha</span><span class="sxs-lookup"><span data-stu-id="58e09-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



