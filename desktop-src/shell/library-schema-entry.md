---
description: Les fichiers de description de bibliothèque sont des fichiers XML qui définissent des bibliothèques.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Schéma de description de la bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104973903"
---
# <a name="library-description-schema"></a><span data-ttu-id="9d067-103">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-103">Library Description Schema</span></span>

<span data-ttu-id="9d067-104">Les fichiers de description de bibliothèque sont des fichiers XML qui définissent des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="9d067-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="9d067-105">Les bibliothèques regroupent les éléments des emplacements de stockage locaux et distants dans une vue unique de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="9d067-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="9d067-106">Les fichiers de description de la bibliothèque suivent le schéma de description de la bibliothèque et sont enregistrés en tant que \* fichiers. Library-ms.</span><span class="sxs-lookup"><span data-stu-id="9d067-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="9d067-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d067-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9d067-108">Vue d’ensemble du schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="9d067-109">Contrôle de version des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9d067-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="9d067-110">Exemple de fichier de description de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="9d067-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d067-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="9d067-112">Vue d’ensemble du schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="9d067-113">Les bibliothèques contiennent des fichiers stockés dans un ou plusieurs emplacements de stockage.</span><span class="sxs-lookup"><span data-stu-id="9d067-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="9d067-114">Les bibliothèques ne stockent pas réellement ces fichiers ; au lieu de cela, ils surveillent les dossiers qui contiennent les fichiers et permettent aux utilisateurs d’accéder aux fichiers et de les organiser de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="9d067-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="9d067-115">Par exemple, un utilisateur peut avoir des fichiers musicaux dans plusieurs dossiers sur un disque dur local et également sur un disque dur externe.</span><span class="sxs-lookup"><span data-stu-id="9d067-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="9d067-116">À l’aide de la **bibliothèque musique**, l’utilisateur peut accéder à tous ces fichiers en même temps et les trier par nom d’artiste ou titre d’album en tant que groupe unique.</span><span class="sxs-lookup"><span data-stu-id="9d067-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="9d067-117">Le schéma de description de la bibliothèque se compose de trois parties majeures, décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="9d067-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d067-118">Informations générales sur la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-118">General library information</span></span> | <span data-ttu-id="9d067-119">Les informations relatives à la bibliothèque, telles que le nom, le propriétaire, la version, l’icône, que l’Explorateur Windows peut utiliser lorsqu’il affiche la bibliothèque à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d067-119">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="9d067-120">Propriétés de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-120">Library properties</span></span>          | <span data-ttu-id="9d067-121">Une ou plusieurs propriétés qui décrivent la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="9d067-121">One or more properties that describe the library.</span></span> <span data-ttu-id="9d067-122">Ces propriétés personnalisées sont spécifiques à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="9d067-122">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="9d067-123">Emplacements de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-123">Library locations</span></span>           | <span data-ttu-id="9d067-124">Un ou plusieurs connecteurs de recherche qui identifient les emplacements de stockage à inclure dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="9d067-124">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="9d067-125">Chacun de ces emplacements peut également avoir un ensemble unique de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9d067-125">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="9d067-126">Les fichiers de bibliothèque de Windows 7 sont stockés dans le dossier connu, FOLDERID \_ Libraries.</span><span class="sxs-lookup"><span data-stu-id="9d067-126">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="9d067-127">Par défaut, le \_ dossier FOLDERID Libraries se trouve dans% UserProfile% \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Libraries.</span><span class="sxs-lookup"><span data-stu-id="9d067-127">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="9d067-128">Contrôle de version des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9d067-128">Namespace Versioning</span></span>

<span data-ttu-id="9d067-129">Les versions du format de fichier de description de la bibliothèque ( \* . Library-ms) sont suivies en modifiant l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="9d067-129">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="9d067-130">Pour Windows 7, le format de fichier est l’espace de noms par défaut suivant : https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="9d067-130">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="9d067-131">Toutefois, les versions du contenu de la bibliothèque sont suivies à l’aide [<version>](schema-library-version.md) de l’élément dans un fichier de description de bibliothèque spécifique.</span><span class="sxs-lookup"><span data-stu-id="9d067-131">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="9d067-132">Exemple de fichier de description de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d067-132">Example of a Library Description File</span></span>

<span data-ttu-id="9d067-133">Voici un exemple de fichier de description de bibliothèque qui définit une bibliothèque pour les fichiers de document.</span><span class="sxs-lookup"><span data-stu-id="9d067-133">The following is an example of a Library Description file that defines a library for document files.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9d067-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d067-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d067-135">Élément folderType (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-135">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="9d067-136">Élément iconReference (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-136">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="9d067-137">Élément isLibraryPinned (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-137">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="9d067-138">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-138">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="9d067-139">Élément Name (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-139">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="9d067-140">Élément ownerSID (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-140">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="9d067-141">Property, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-141">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="9d067-142">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="9d067-143">Élément searchConnectorDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="9d067-144">Élément searchConnectorDescriptionList (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="9d067-145">Élément templateInfo (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="9d067-146">version, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="9d067-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="9d067-147">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="9d067-147">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
