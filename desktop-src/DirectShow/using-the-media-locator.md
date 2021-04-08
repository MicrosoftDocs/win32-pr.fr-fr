---
description: Utilisation du localisateur de média
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Utilisation du localisateur de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953347"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="406b7-103">Utilisation du localisateur de média</span><span class="sxs-lookup"><span data-stu-id="406b7-103">Using the Media Locator</span></span>

<span data-ttu-id="406b7-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="406b7-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="406b7-105">Le localisateur de média est un objet d’assistance qui vérifie les noms de fichiers et recherche les fichiers manquants dans les répertoires locaux ou réseau.</span><span class="sxs-lookup"><span data-stu-id="406b7-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="406b7-106">Le détecteur de média conserve un cache de chemins d’accès aux répertoires dans lesquels il a trouvé des fichiers dans les recherches précédentes.</span><span class="sxs-lookup"><span data-stu-id="406b7-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="406b7-107">Pour localiser un fichier, il effectue une recherche dans les répertoires de son cache.</span><span class="sxs-lookup"><span data-stu-id="406b7-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="406b7-108">En cas d’échec, le détecteur de média peut afficher une boîte de dialogue Ouvrir un fichier pour permettre à l’utilisateur de localiser un fichier manuellement.</span><span class="sxs-lookup"><span data-stu-id="406b7-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="406b7-109">En supposant que l’utilisateur trouve le fichier, le localisateur de média ajoute le nouveau répertoire à son cache.</span><span class="sxs-lookup"><span data-stu-id="406b7-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="406b7-110">Le localisateur de média expose l’interface [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="406b7-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="406b7-111">En règle générale, votre application ne crée pas directement une instance du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="406b7-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="406b7-112">Au lieu de cela, la chronologie et le moteur de rendu fournissent les méthodes suivantes pour valider les noms de fichiers à l’aide du détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="406b7-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="406b7-113">Pour valider des noms de fichiers dans la chronologie, appelez [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span><span class="sxs-lookup"><span data-stu-id="406b7-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="406b7-114">Si vous le souhaitez, cette méthode met également à jour les objets sources avec les noms de fichiers corrects.</span><span class="sxs-lookup"><span data-stu-id="406b7-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="406b7-115">Pour valider des noms de fichiers lors du rendu du projet, appelez [**IRenderEngine :: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span><span class="sxs-lookup"><span data-stu-id="406b7-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="406b7-116">Les deux méthodes prennent des indicateurs qui contrôlent le comportement du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="406b7-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="406b7-117">Par exemple, vous pouvez limiter la recherche aux répertoires locaux.</span><span class="sxs-lookup"><span data-stu-id="406b7-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="406b7-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="406b7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="406b7-119">Utilisation des sources</span><span class="sxs-lookup"><span data-stu-id="406b7-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



