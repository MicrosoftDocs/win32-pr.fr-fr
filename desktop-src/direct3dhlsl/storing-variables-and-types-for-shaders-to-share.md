---
title: Stockage des variables et des types pour les nuanceurs à partager
description: L’objet de liaison de classe est un espace de noms pour les variables et les types que plusieurs nuanceurs peuvent partager.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971783"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="6a9d2-103">Stockage des variables et des types pour les nuanceurs à partager</span><span class="sxs-lookup"><span data-stu-id="6a9d2-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="6a9d2-104">L’objet de liaison de classe est un espace de noms pour les variables et les types que plusieurs nuanceurs peuvent partager.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="6a9d2-105">Quand vous transmettez un objet de liaison de classe dans un appel pour créer un nuanceur, le runtime recueille une liste de variables et de types qui peuvent implémenter chaque interface dans le nuanceur et stocke les noms de ces variables et types dans l’objet de liaison de classe.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="6a9d2-106">Par conséquent, lorsque vous appelez la méthode [**ID3D11ClassLinkage :: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) pour générer des instances de classe à partir de l’objet de liaison de classe, le runtime peut récupérer la variable ou le type qui correspond au nom fourni dans chaque nuanceur (si ce nom est valide pour un nuanceur donné) et qui est créé avec l’objet de liaison de classe donné.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="6a9d2-107">Par exemple, supposons que vous avez une classe **Light** qui implémente une interface de **couleur** , et que vous utilisez cette classe dans votre nuanceur de sommets et votre nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="6a9d2-108">Quand vous créez un nuanceur (par exemple, en appelant [**ID3D11Device :: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), le runtime détermine que le type de classe **Light** est disponible dans les nuanceurs vertex et pixel et ajoute le type de classe **Light** à l’objet de liaison de classe.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="6a9d2-109">Vous pouvez ensuite créer une instance de **lumière** à l’emplacement de votre choix, lier les ressources pour les deux nuanceurs et passer cette instance dans le tableau d’instances de classe lorsque vous définissez le nuanceur sur l’appareil (par exemple, en appelant [**ID3D11DeviceContext ::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span><span class="sxs-lookup"><span data-stu-id="6a9d2-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="6a9d2-110">Le runtime exécute ensuite la séquence suivante :</span><span class="sxs-lookup"><span data-stu-id="6a9d2-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="6a9d2-111">Vérifie que l’instance a été créée avec le même objet de liaison de classe.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="6a9d2-112">Vérifie que le type de classe **Light** est disponible dans les nuanceurs de sommets et de pixels.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="6a9d2-113">Sélectionne les tables de fonctions appropriées, qui peuvent être différentes pour les nuanceurs vertex et pixel.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="6a9d2-114">Envoie les offsets fournis par l’instance.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="6a9d2-115">L’objet de liaison de classe est finalement un référentiel de noms de type et de variable.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="6a9d2-116">Le nombre maximal de noms disponibles pour chaque élément (type et variable) est de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="6a9d2-117">Plus les noms de type et de variable sont longs, plus l’exigence de stockage est importante pour les métadonnées d’interface stockées par nuanceur.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="6a9d2-118">Cela est dû au fait que le runtime doit stocker un mappage pour ces noms pour chaque nuanceur.</span><span class="sxs-lookup"><span data-stu-id="6a9d2-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a9d2-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a9d2-119">Related Topics</span></span>

[<span data-ttu-id="6a9d2-120">Liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="6a9d2-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="6a9d2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a9d2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a9d2-122">Liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="6a9d2-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 