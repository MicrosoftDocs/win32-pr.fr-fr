---
description: Cette rubrique décrit une nouvelle vue dans l’Explorateur Windows, appelée affichage du contenu, qui affiche le contenu le plus pertinent pour chaque élément.
title: Affichage du contenu par type de fichier ou par type
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757360"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="06a46-103">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="06a46-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="06a46-104">Cette rubrique décrit une nouvelle vue dans l’Explorateur Windows, appelée affichage du contenu, qui affiche le contenu le plus pertinent pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="06a46-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="06a46-105">À l’aide d’un ensemble de clés de Registre, les éléments peuvent définir une liste de propriétés et une disposition que l’interpréteur de commandes utilise pour la vue de contenu.</span><span class="sxs-lookup"><span data-stu-id="06a46-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="06a46-106">L’interpréteur de commandes récupère les clés de Registre à l’aide du [tableau d’association](fa-perceivedtypes.md)de l’élément.</span><span class="sxs-lookup"><span data-stu-id="06a46-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="06a46-107">Comment fonctionne l’affichage du contenu ?</span><span class="sxs-lookup"><span data-stu-id="06a46-107">How Does the Content View Work?</span></span>

<span data-ttu-id="06a46-108">Dans Windows 7 et versions ultérieures, l’affichage du contenu utilise une logique de redimensionnement qui supprime les propriétés lorsque la taille de la fenêtre diminue, pour s’assurer que les propriétés les plus critiques ont encore de la place pour être clairement lisibles.</span><span class="sxs-lookup"><span data-stu-id="06a46-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="06a46-109">La capture d’écran suivante illustre l’affichage du contenu des résultats de recherche contenant de la musique, des images et des documents.</span><span class="sxs-lookup"><span data-stu-id="06a46-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![affichage du contenu des résultats de la recherche contenant de la musique, des images et des documents](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="06a46-111">Certaines sources de données de l’interpréteur de commandes utilisent l’affichage du contenu par défaut, mais les utilisateurs peuvent sélectionner l’affichage du contenu en cliquant sur le bouton **afficher le contrôle** dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="06a46-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="06a46-112">Une source de données Shell étend l’espace de noms Shell et expose des éléments dans un magasin de données.</span><span class="sxs-lookup"><span data-stu-id="06a46-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="06a46-113">Les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="06a46-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="06a46-114">Comment implémenter l’affichage du contenu</span><span class="sxs-lookup"><span data-stu-id="06a46-114">How to Implement the Content View</span></span>

<span data-ttu-id="06a46-115">Lors de l’inscription d’un nouveau [type de fichier](fa-file-types.md) ou [Gestionnaire de protocole](../search/-search-3x-wds-extidx-prot-implementing.md), vous pouvez tirer parti de l’affichage de contenu à l’aide de l’une des deux approches.</span><span class="sxs-lookup"><span data-stu-id="06a46-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="06a46-116">Vous pouvez utiliser un ensemble de propriétés et un modèle de disposition existants, ou vous pouvez créer votre propre combinaison.</span><span class="sxs-lookup"><span data-stu-id="06a46-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="06a46-117">Vous pouvez utiliser une entrée de Registre pour associer votre type de fichier ou élément à un [type](../properties/building-property-handlers-user-friendly-kind-names.md)prédéfini, qui est une propriété que vous pouvez considérer comme une catégorie de contenu.</span><span class="sxs-lookup"><span data-stu-id="06a46-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="06a46-118">En associant votre type de fichier ou élément à certains de ces genres, vous héritez automatiquement des modèles de disposition de vue de contenu et des listes de propriétés de ce type.</span><span class="sxs-lookup"><span data-stu-id="06a46-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="06a46-119">Windows définit les modèles de disposition de vue de contenu et les listes de propriétés pour les types suivants : documents, courrier électronique, dossier, musique, image et générique.</span><span class="sxs-lookup"><span data-stu-id="06a46-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="06a46-120">Ce type d’association est encouragé.</span><span class="sxs-lookup"><span data-stu-id="06a46-120">This type of association is encouraged.</span></span> <span data-ttu-id="06a46-121">Elle vous permet de fournir une expérience cohérente qu’un utilisateur attend pour des éléments similaires.</span><span class="sxs-lookup"><span data-stu-id="06a46-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="06a46-122">Pour plus d’informations, consultez [types de fichiers](fa-file-types.md) et [noms](../properties/building-property-handlers-user-friendly-kind-names.md) de types et [comment inscrire un ensemble de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span><span class="sxs-lookup"><span data-stu-id="06a46-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06a46-123">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="06a46-123">Additional Resources</span></span>

-   <span data-ttu-id="06a46-124">Pour obtenir une documentation de référence sur les propriétés, consultez [System. Kind](../properties/props-system-kind.md)et [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="06a46-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="06a46-125">Pour obtenir une documentation de référence PropList, consultez [System. PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)et [System. PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span><span class="sxs-lookup"><span data-stu-id="06a46-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06a46-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06a46-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a46-127">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="06a46-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="06a46-128">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="06a46-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="06a46-129">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="06a46-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="06a46-130">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="06a46-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="06a46-131">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="06a46-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="06a46-132">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="06a46-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="06a46-133">Types perçus</span><span class="sxs-lookup"><span data-stu-id="06a46-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="06a46-134">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="06a46-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
