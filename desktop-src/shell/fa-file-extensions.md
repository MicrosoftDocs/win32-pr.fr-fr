---
description: L’inscription d’un type de fichier est la première étape de la création d’une association de fichiers, ce qui rend ce type de fichier &\# 0034 ; connu&\# 0034 ; dans le shell. Toutefois, sans gestionnaires de type de fichier, l’interpréteur de commandes ne peut pas exposer d’informations à l’utilisateur à partir du fichier.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Gestionnaires de types de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862366"
---
# <a name="file-type-handlers"></a><span data-ttu-id="7403a-104">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="7403a-104">File Type Handlers</span></span>

<span data-ttu-id="7403a-105">L' [inscription d’un type de fichier](fa-how-work.md) est la première étape de la création d’une association de fichiers, ce qui rend ce type de fichier « connu » pour l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="7403a-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="7403a-106">Toutefois, sans gestionnaires de type de fichier, l’interpréteur de commandes ne peut pas exposer d’informations à l’utilisateur à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="7403a-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="7403a-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="7403a-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7403a-108">Rendre un type de fichier connu de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="7403a-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="7403a-109">Description du gestionnaire de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="7403a-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="7403a-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7403a-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="7403a-111">Rendre un type de fichier connu de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="7403a-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="7403a-112">Dans la capture d’écran suivante de l’Explorateur Windows, le fichier image désert. connu apparaît dans la bibliothèque d' **images** de Shell et est associé uniquement à l’application Paint.</span><span class="sxs-lookup"><span data-stu-id="7403a-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![capture d’écran montrant l’Explorateur ouverture d’une image sans type de fichier](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="7403a-114">Le fichier désert. connu dans la capture d’écran précédente ne dispose pas des fonctionnalités suivantes qui sont activées par un gestionnaire de type de fichier :</span><span class="sxs-lookup"><span data-stu-id="7403a-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="7403a-115">Miniature ou aperçu</span><span class="sxs-lookup"><span data-stu-id="7403a-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="7403a-116">Verbes spécifiques à une image dans le menu contextuel, par exemple :</span><span class="sxs-lookup"><span data-stu-id="7403a-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="7403a-117">Faire pivoter l’aperçu</span><span class="sxs-lookup"><span data-stu-id="7403a-117">Rotate Preview</span></span>
    -   <span data-ttu-id="7403a-118">Définir comme arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="7403a-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="7403a-119">Imprimer</span><span class="sxs-lookup"><span data-stu-id="7403a-119">Print</span></span>
-   <span data-ttu-id="7403a-120">Propriétés propres à l’image dans le volet d' **informations** , par exemple :</span><span class="sxs-lookup"><span data-stu-id="7403a-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="7403a-121">Date de prise</span><span class="sxs-lookup"><span data-stu-id="7403a-121">Date Taken</span></span>
    -   <span data-ttu-id="7403a-122">Balises</span><span class="sxs-lookup"><span data-stu-id="7403a-122">Tags</span></span>
    -   <span data-ttu-id="7403a-123">Rating</span><span class="sxs-lookup"><span data-stu-id="7403a-123">Rating</span></span>
-   <span data-ttu-id="7403a-124">Indexation du texte de fichier</span><span class="sxs-lookup"><span data-stu-id="7403a-124">Indexing of file text</span></span>

<span data-ttu-id="7403a-125">Dans la capture d’écran suivante, le même fichier (désert. connu) a l’extension. jpg, qui est un type de fichier inscrit qui est associé à des gestionnaires de types de fichiers. ainsi, une image miniature et davantage de propriétés sont affichées.</span><span class="sxs-lookup"><span data-stu-id="7403a-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![image avec un type de fichier inscrit et les gestionnaires de types de fichiers associés](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="7403a-127">Description du gestionnaire de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="7403a-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="7403a-128">La fonctionnalité fournie par chaque gestionnaire de type de fichier est présentée dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="7403a-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="7403a-129">Handler</span><span class="sxs-lookup"><span data-stu-id="7403a-129">Handler</span></span>                                                      | <span data-ttu-id="7403a-130">Description</span><span class="sxs-lookup"><span data-stu-id="7403a-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7403a-131">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="7403a-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="7403a-132">Un gestionnaire de menu contextuel, parfois appelé gestionnaire de menu contextuel, est un gestionnaire de type de fichier qui ajoute des commandes à un menu contextuel existant.</span><span class="sxs-lookup"><span data-stu-id="7403a-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="7403a-133">Ces gestionnaires sont associés à un type de fichier particulier et sont appelés à chaque fois qu’un menu contextuel est affiché pour un membre du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="7403a-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7403a-134">Vidéo miniature</span><span class="sxs-lookup"><span data-stu-id="7403a-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="7403a-135">Gestionnaire qui fournit une image pour représenter un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="7403a-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="7403a-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="7403a-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="7403a-137">Gestionnaire de propriétés qui fournit l’accès aux propriétés de l’élément pour Windows Search, l’Explorateur Windows et d’autres applications qui ont besoin d’accéder aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="7403a-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7403a-138">Préversion</span><span class="sxs-lookup"><span data-stu-id="7403a-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="7403a-139">Gestionnaire qui produit rapidement une vue simplifiée en lecture seule de l’élément à afficher dans le volet de visualisation de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7403a-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="7403a-140">Filtres</span><span class="sxs-lookup"><span data-stu-id="7403a-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="7403a-141">Un filtre, une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , qui analyse des documents pour le texte et les propriétés (également appelés attributs).</span><span class="sxs-lookup"><span data-stu-id="7403a-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="7403a-142">Il extrait des segments de texte à partir de ces documents, en filtrant la mise en forme incorporée et en conservant les informations relatives à la position du texte.</span><span class="sxs-lookup"><span data-stu-id="7403a-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="7403a-143">Il extrait également des blocs de valeurs, qui sont des propriétés d’un document entier ou de parties bien définies d’un document.</span><span class="sxs-lookup"><span data-stu-id="7403a-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="7403a-144">**IFilter** fournit la base pour la création d’applications de niveau supérieur, telles que les indexeurs de documents et les visionneuses indépendantes des applications.</span><span class="sxs-lookup"><span data-stu-id="7403a-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7403a-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7403a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7403a-146">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="7403a-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="7403a-147">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="7403a-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="7403a-148">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="7403a-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="7403a-149">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="7403a-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="7403a-150">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="7403a-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="7403a-151">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="7403a-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="7403a-152">Types perçus</span><span class="sxs-lookup"><span data-stu-id="7403a-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="7403a-153">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="7403a-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
