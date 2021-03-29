---
description: Un type perçu est une catégorie de types de fichiers qui vous permet d’identifier votre type de fichier sur Windows (et les applications) comme une image, un fichier audio, un document ou tout autre type.
title: Types perçus (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991861"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="e9acd-103">Types perçus (shell Windows)</span><span class="sxs-lookup"><span data-stu-id="e9acd-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="e9acd-104">Un type perçu est une catégorie de types de fichiers qui vous permet d’identifier votre type de fichier sur Windows (et les applications) comme une image, un fichier audio, un document ou tout autre type.</span><span class="sxs-lookup"><span data-stu-id="e9acd-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="e9acd-105">Les types perçus sont utilisés à plusieurs fins, notamment la détermination du type de dossier, qui est ensuite utilisé pour définir les paramètres d’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9acd-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="e9acd-106">Par exemple, un dossier contenant des fichiers dont l’image est de type perçue reçoit un mode d’affichage par défaut de miniatures.</span><span class="sxs-lookup"><span data-stu-id="e9acd-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="e9acd-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9acd-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e9acd-108">À propos des types perçus</span><span class="sxs-lookup"><span data-stu-id="e9acd-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="e9acd-109">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e9acd-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="e9acd-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9acd-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="e9acd-111">À propos des types perçus</span><span class="sxs-lookup"><span data-stu-id="e9acd-111">About Perceived Types</span></span>

<span data-ttu-id="e9acd-112">Les types perçus, définis en tant que valeurs PerceivedType, sont similaires aux types de fichiers, à ceci près qu’ils font référence à des catégories larges de types de fichiers plutôt qu’à des types de fichiers spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e9acd-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="e9acd-113">Par exemple, l’image, le texte, l’audio et la compression sont des types perçus.</span><span class="sxs-lookup"><span data-stu-id="e9acd-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="e9acd-114">Les types de fichiers (généralement des types de fichiers publics) peuvent être affectés à un type perçu et doivent toujours être affectés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e9acd-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="e9acd-115">Par exemple, les types de fichiers image. bmp,. png,. jpg et. gif sont également perçus comme une image de type.</span><span class="sxs-lookup"><span data-stu-id="e9acd-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="e9acd-116">Les types perçus par défaut sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e9acd-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="e9acd-117">Dossier</span><span class="sxs-lookup"><span data-stu-id="e9acd-117">Folder</span></span>
-   <span data-ttu-id="e9acd-118">Texte</span><span class="sxs-lookup"><span data-stu-id="e9acd-118">Text</span></span>
-   <span data-ttu-id="e9acd-119">Image</span><span class="sxs-lookup"><span data-stu-id="e9acd-119">Image</span></span>
-   <span data-ttu-id="e9acd-120">Audio</span><span class="sxs-lookup"><span data-stu-id="e9acd-120">Audio</span></span>
-   <span data-ttu-id="e9acd-121">Vidéo</span><span class="sxs-lookup"><span data-stu-id="e9acd-121">Video</span></span>
-   <span data-ttu-id="e9acd-122">Compressé</span><span class="sxs-lookup"><span data-stu-id="e9acd-122">Compressed</span></span>
-   <span data-ttu-id="e9acd-123">Document</span><span class="sxs-lookup"><span data-stu-id="e9acd-123">Document</span></span>
-   <span data-ttu-id="e9acd-124">Système</span><span class="sxs-lookup"><span data-stu-id="e9acd-124">System</span></span>
-   <span data-ttu-id="e9acd-125">Application</span><span class="sxs-lookup"><span data-stu-id="e9acd-125">Application</span></span>
-   <span data-ttu-id="e9acd-126">Gamemedia</span><span class="sxs-lookup"><span data-stu-id="e9acd-126">Gamemedia</span></span>
-   <span data-ttu-id="e9acd-127">Contacts</span><span class="sxs-lookup"><span data-stu-id="e9acd-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9acd-128">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e9acd-128">Additional Resources</span></span>

-   <span data-ttu-id="e9acd-129">Pour plus d’informations sur l’enregistrement des types perçus, consultez [inscription des applications](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="e9acd-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="e9acd-130">Pour obtenir la liste des types perçus par défaut, consultez l’énumération [**perçue**](/windows/win32/api/shtypes/ne-shtypes-perceived) .</span><span class="sxs-lookup"><span data-stu-id="e9acd-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="e9acd-131">Pour récupérer le type perçu d’un fichier en fonction de son extension de nom de fichier, consultez la fonction [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .</span><span class="sxs-lookup"><span data-stu-id="e9acd-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9acd-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9acd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9acd-133">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="e9acd-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="e9acd-134">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="e9acd-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="e9acd-135">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="e9acd-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="e9acd-136">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="e9acd-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="e9acd-137">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="e9acd-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="e9acd-138">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="e9acd-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="e9acd-139">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="e9acd-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="e9acd-140">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="e9acd-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



