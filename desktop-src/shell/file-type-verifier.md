---
description: Le vérificateur de type de fichier est un outil qui permet aux éditeurs de logiciels indépendants (ISV) de vérifier que leurs types de fichiers uniques sont correctement implémentés.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Vérificateur de type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864949"
---
# <a name="file-type-verifier"></a><span data-ttu-id="1ade5-103">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ade5-103">File Type Verifier</span></span>

<span data-ttu-id="1ade5-104">Le vérificateur de type de fichier est un outil qui permet aux éditeurs de logiciels indépendants (ISV) de vérifier que leurs types de fichiers uniques sont correctement implémentés.</span><span class="sxs-lookup"><span data-stu-id="1ade5-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="1ade5-105">Les implémentations de haute qualité de vos gestionnaires de types de fichiers sont cruciales pour une expérience utilisateur optimale, car les utilisateurs interagissent avec votre format de fichier de nombreuses façons dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="1ade5-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="1ade5-106">Les utilisateurs peuvent effectuer des recherches en texte intégral, Trier par métadonnées personnalisées ou afficher des miniatures et des aperçus enrichis de votre format de fichier.</span><span class="sxs-lookup"><span data-stu-id="1ade5-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="1ade5-107">Pour obtenir des instructions sur l’utilisation du vérificateur de type de fichier, consultez la page [utilisation du vérificateur de type de fichier](how-to-use-the-file-type-verifier.md).</span><span class="sxs-lookup"><span data-stu-id="1ade5-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="1ade5-108">À propos de l’outil de vérification de type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ade5-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="1ade5-109">Le vérificateur de type de fichier est un programme qui est disponible dans le cadre du [Kit de développement logiciel (SDK) Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1ade5-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1ade5-110">Il est conçu pour aider les développeurs qui créent des [types de fichiers](fa-file-types.md) Windows personnalisés à détecter les problèmes potentiels liés à leurs types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1ade5-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="1ade5-111">Bien que le vérificateur de type de fichier s’exécute uniquement sur Windows 7 et versions ultérieures, les règles appliquées par le vérificateur de type de fichier s’appliquent à toutes les versions de Windows où les fonctionnalités qu’il vérifie sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="1ade5-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="1ade5-112">Le vérificateur de type de fichier exécute plusieurs tests sur le type de fichier pour vérifier qu’il est correctement inscrit, et qu’il fournit les [gestionnaires de types de fichiers](fa-file-extensions.md) appropriés pour afficher correctement le type de fichier dans l’Explorateur Windows et, le cas échéant, qu’il prend en charge l’indexation du contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="1ade5-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="1ade5-113">Le vérificateur de type de fichier teste les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1ade5-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="1ade5-114">Gestionnaires d’aperçus</span><span class="sxs-lookup"><span data-stu-id="1ade5-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="1ade5-115">Gestionnaires de miniatures</span><span class="sxs-lookup"><span data-stu-id="1ade5-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="1ade5-116">Gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="1ade5-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="1ade5-117">Gestionnaires de verbes</span><span class="sxs-lookup"><span data-stu-id="1ade5-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="1ade5-118">Filtres (IFilter)</span><span class="sxs-lookup"><span data-stu-id="1ade5-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="1ade5-119">Associations de genres</span><span class="sxs-lookup"><span data-stu-id="1ade5-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="1ade5-120">Types perçus</span><span class="sxs-lookup"><span data-stu-id="1ade5-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="1ade5-121">Propriétés importantes</span><span class="sxs-lookup"><span data-stu-id="1ade5-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="1ade5-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ade5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ade5-123">Utilisation du vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="1ade5-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="1ade5-124">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="1ade5-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="1ade5-125">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="1ade5-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="1ade5-126">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="1ade5-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="1ade5-127">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="1ade5-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="1ade5-128">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="1ade5-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="1ade5-129">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="1ade5-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="1ade5-130">Types perçus</span><span class="sxs-lookup"><span data-stu-id="1ade5-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="1ade5-131">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="1ade5-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
