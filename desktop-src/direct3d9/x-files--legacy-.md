---
description: Le format de fichier X fait référence aux fichiers portant l’extension de nom de fichier. X.
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: Fichiers X (hérité) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845950"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="466d5-103">Fichiers X (hérité) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="466d5-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="466d5-104">Le format de fichier X fait référence aux fichiers portant l’extension de nom de fichier. X.</span><span class="sxs-lookup"><span data-stu-id="466d5-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="466d5-105">X ont été introduits avec DirectX 2,0.</span><span class="sxs-lookup"><span data-stu-id="466d5-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="466d5-106">Une version binaire de ce format a été publiée par la suite avec DirectX 3,0, qui est également décrit dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="466d5-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="466d5-107">DirectX 6,0 a introduit des interfaces et des méthodes qui permettent de lire et d’écrire dans des fichiers. x.</span><span class="sxs-lookup"><span data-stu-id="466d5-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="466d5-108">Les fichiers X fournissent un format piloté par des modèles qui permet le stockage de maillages, de textures, d’animations et d’objets définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="466d5-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="466d5-109">La prise en charge des jeux d’animations vous permet de stocker des chemins prédéfinis pour la lecture en temps réel.</span><span class="sxs-lookup"><span data-stu-id="466d5-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="466d5-110">L’instanciation et les hiérarchies sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="466d5-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="466d5-111">L’instanciation active plusieurs références à un objet, par exemple une maille, tout en stockant ses données une seule fois par fichier.</span><span class="sxs-lookup"><span data-stu-id="466d5-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="466d5-112">Les hiérarchies permettent d’exprimer des relations entre les enregistrements de données.</span><span class="sxs-lookup"><span data-stu-id="466d5-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="466d5-113">Le format de fichier. x fournit des primitives de données de bas niveau sur lesquelles les applications définissent des primitives de niveau supérieur par le biais de modèles.</span><span class="sxs-lookup"><span data-stu-id="466d5-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="466d5-114">Les modèles en trois dimensions créés dans les applications Maya 3ds Max ou Alias Wavefront de l’alias \| peuvent être convertis en fichiers. x avec les extensions DirectX pour l’alias Maya.</span><span class="sxs-lookup"><span data-stu-id="466d5-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="466d5-115">Cette section décrit la structure des fichiers. x et explique comment les utiliser dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="466d5-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="466d5-116">Les informations sont réparties dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="466d5-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="466d5-117">Chargement d’un fichier X (hérité) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="466d5-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="466d5-118">Enregistrement dans un fichier X (hérité) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="466d5-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="466d5-119">Définition d’un cube simple (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="466d5-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="466d5-120">Ajout de textures (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="466d5-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="466d5-121">Ajout de frames et d’animations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="466d5-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="466d5-122">Pour plus d’informations sur le format de fichier. x, consultez [référence de fichier x](dx9-graphics-reference-d3dx-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="466d5-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="466d5-123">Pour plus d’informations sur l’API de fichier. x, consultez [référence de fichier x (hérité)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="466d5-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="466d5-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="466d5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="466d5-125">Prise en main</span><span class="sxs-lookup"><span data-stu-id="466d5-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



