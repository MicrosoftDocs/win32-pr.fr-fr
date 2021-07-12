---
description: Les fichiers de description de bibliothèque sont des fichiers XML qui définissent des bibliothèques.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Schéma de description de la bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a6da99820e81c55e5d705c72d4d0509ea271a4a
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581737"
---
# <a name="library-description-schema"></a><span data-ttu-id="d8d10-103">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-103">Library Description Schema</span></span>

<span data-ttu-id="d8d10-104">Les fichiers de description de bibliothèque sont des fichiers XML qui définissent des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="d8d10-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="d8d10-105">les bibliothèques regroupent les éléments des emplacements de stockage locaux et distants dans un affichage unique dans Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d8d10-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="d8d10-106">Les fichiers de description de la bibliothèque suivent le schéma de description de la bibliothèque et sont enregistrés en tant que \* fichiers. Library-ms.</span><span class="sxs-lookup"><span data-stu-id="d8d10-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="d8d10-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8d10-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d8d10-108">Vue d’ensemble du schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="d8d10-109">Contrôle de version des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d8d10-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="d8d10-110">Exemple de fichier de description de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="d8d10-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8d10-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="d8d10-112">Vue d’ensemble du schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="d8d10-113">Les bibliothèques contiennent des fichiers stockés dans un ou plusieurs emplacements de stockage.</span><span class="sxs-lookup"><span data-stu-id="d8d10-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="d8d10-114">Les bibliothèques ne stockent pas réellement ces fichiers ; au lieu de cela, ils surveillent les dossiers qui contiennent les fichiers et permettent aux utilisateurs d’accéder aux fichiers et de les organiser de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="d8d10-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="d8d10-115">Par exemple, un utilisateur peut avoir des fichiers musicaux dans plusieurs dossiers sur un disque dur local et également sur un disque dur externe.</span><span class="sxs-lookup"><span data-stu-id="d8d10-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="d8d10-116">à l’aide de la **bibliothèque de Musique**, l’utilisateur peut accéder à tous ces fichiers en même temps et les trier par nom d’artiste ou titre d’album en tant que groupe unique.</span><span class="sxs-lookup"><span data-stu-id="d8d10-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="d8d10-117">Le schéma de description de la bibliothèque se compose de trois parties majeures, décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="d8d10-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



| <span data-ttu-id="d8d10-118">Partie</span><span class="sxs-lookup"><span data-stu-id="d8d10-118">Part</span></span>                        | <span data-ttu-id="d8d10-119">Description</span><span class="sxs-lookup"><span data-stu-id="d8d10-119">Description</span></span>                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d10-120">Informations générales sur la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-120">General library information</span></span> | <span data-ttu-id="d8d10-121">informations sur la bibliothèque, telles que le nom, le propriétaire, la version, l’icône, que Windows explorateur peut utiliser lorsqu’il affiche la bibliothèque à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d8d10-121">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="d8d10-122">Propriétés de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-122">Library properties</span></span>          | <span data-ttu-id="d8d10-123">Une ou plusieurs propriétés qui décrivent la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d8d10-123">One or more properties that describe the library.</span></span> <span data-ttu-id="d8d10-124">Ces propriétés personnalisées sont spécifiques à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d8d10-124">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="d8d10-125">Emplacements de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-125">Library locations</span></span>           | <span data-ttu-id="d8d10-126">Un ou plusieurs connecteurs de recherche qui identifient les emplacements de stockage à inclure dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d8d10-126">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="d8d10-127">Chacun de ces emplacements peut également avoir un ensemble unique de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8d10-127">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="d8d10-128">les fichiers de bibliothèque dans Windows 7 sont stockés dans le dossier connu, FOLDERID \_ libraries.</span><span class="sxs-lookup"><span data-stu-id="d8d10-128">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="d8d10-129">par défaut, le \_ dossier FOLDERID libraries se trouve dans% USERPROFILE% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ libraries.</span><span class="sxs-lookup"><span data-stu-id="d8d10-129">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="d8d10-130">Contrôle de version des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d8d10-130">Namespace Versioning</span></span>

<span data-ttu-id="d8d10-131">Les versions du format de fichier de description de la bibliothèque ( \* . Library-ms) sont suivies en modifiant l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d8d10-131">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="d8d10-132">pour Windows 7, le format de fichier est l’espace de noms par défaut suivant : https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="d8d10-132">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="d8d10-133">Toutefois, les versions du contenu de la bibliothèque sont suivies à l’aide [<version>](schema-library-version.md) de l’élément dans un fichier de description de bibliothèque spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8d10-133">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="d8d10-134">Exemple de fichier de description de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d10-134">Example of a Library Description File</span></span>

<span data-ttu-id="d8d10-135">Voici un exemple de fichier de description de bibliothèque qui définit une bibliothèque pour les fichiers de document.</span><span class="sxs-lookup"><span data-stu-id="d8d10-135">The following is an example of a Library Description file that defines a library for document files.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="d8d10-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8d10-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8d10-137">Élément folderType (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-137">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="d8d10-138">Élément iconReference (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-138">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="d8d10-139">Élément isLibraryPinned (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-139">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="d8d10-140">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-140">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="d8d10-141">Élément Name (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-141">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="d8d10-142">Élément ownerSID (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-142">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="d8d10-143">Property, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-143">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="d8d10-144">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-144">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="d8d10-145">Élément searchConnectorDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-145">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="d8d10-146">Élément searchConnectorDescriptionList (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-146">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="d8d10-147">Élément templateInfo (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-147">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="d8d10-148">version, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="d8d10-148">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="d8d10-149">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="d8d10-149">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
