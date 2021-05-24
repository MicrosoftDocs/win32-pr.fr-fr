---
description: Dans Direct3D 10, les ressources de texture sont accessibles à l’aide d’une vue, qui est un mécanisme d’interprétation matérielle d’une ressource en mémoire.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Affichages de texture (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83dd83b1a3896637ce73505de00027ea9dfadac4
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335583"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="56b04-103">Affichages de texture (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="56b04-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="56b04-104">Dans Direct3D 10, les ressources de texture sont accessibles à l’aide d’une vue, qui est un mécanisme d’interprétation matérielle d’une ressource en mémoire.</span><span class="sxs-lookup"><span data-stu-id="56b04-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="56b04-105">Une vue permet à une étape de pipeline particulière d’accéder uniquement aux sous- [ressources](d3d10-graphics-programming-guide-resources-types.md) dont elle a besoin, dans la représentation souhaitée par l’application.</span><span class="sxs-lookup"><span data-stu-id="56b04-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="56b04-106">Une vue prend en charge la notion de ressource sans type.</span><span class="sxs-lookup"><span data-stu-id="56b04-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="56b04-107">Une ressource sans type est une ressource créée avec une taille spécifique, mais pas un type de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="56b04-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="56b04-108">Les données sont interprétées dynamiquement lorsqu’elles sont liées au pipeline.</span><span class="sxs-lookup"><span data-stu-id="56b04-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="56b04-109">L’illustration suivante montre un exemple de liaison d’un tableau de texture 2D avec 6 textures en tant que ressource de nuanceur en créant une vue de ressource de nuanceur pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="56b04-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="56b04-110">La ressource est ensuite traitée comme un tableau de textures.</span><span class="sxs-lookup"><span data-stu-id="56b04-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="56b04-111">(Remarque : une sous-ressource ne peut pas être liée à la fois en entrée et en sortie au pipeline simultanément.)</span><span class="sxs-lookup"><span data-stu-id="56b04-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![illustration d’un tableau de textures avec six textures](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="56b04-113">Lors de l’utilisation d’un tableau de texture 2D en tant que cible de rendu, la ressource peut être affichée sous la forme d’un tableau de textures 2D (6 dans cet exemple) avec des niveaux de mipmap (3 dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="56b04-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="56b04-114">Créez un objet de vue pour une cible de rendu en appelant CreateRenderTargetView.</span><span class="sxs-lookup"><span data-stu-id="56b04-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="56b04-115">Appelez ensuite OMSetRenderTargets pour définir la vue de la cible de rendu sur le pipeline.</span><span class="sxs-lookup"><span data-stu-id="56b04-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="56b04-116">Affichez les cibles de rendu en appelant Draw et en utilisant le RenderTargetArrayIndex pour indexer dans la texture appropriée dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="56b04-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="56b04-117">Vous pouvez utiliser une sous-ressource (un niveau de mipmap, une combinaison d’index de tableau) pour effectuer une liaison à n’importe quel tableau de sous-ressources.</span><span class="sxs-lookup"><span data-stu-id="56b04-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="56b04-118">Vous pouvez donc effectuer une liaison avec le deuxième niveau de mipmap et mettre à jour ce niveau de mipmap particulier uniquement si vous le souhaitez, comme dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="56b04-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![illustration de la liaison uniquement au deuxième niveau de mipmap d’un tableau de texture](images/d3d10-cube-texture-faces-subresource.png)



<span data-ttu-id="56b04-120">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="56b04-120">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="56b04-121">Dans Direct3D 10, vous ne liez plus une ressource directement au pipeline, vous créez une vue d’une ressource, puis vous définissez la vue sur le pipeline.</span><span class="sxs-lookup"><span data-stu-id="56b04-121">In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="56b04-122">Cela permet la validation et le mappage dans le runtime et le pilote pour se produire lors de la création de la vue, réduisant ainsi la vérification du type au moment de la liaison.</span><span class="sxs-lookup"><span data-stu-id="56b04-122">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="56b04-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56b04-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b04-124">Ressources (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="56b04-124">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




