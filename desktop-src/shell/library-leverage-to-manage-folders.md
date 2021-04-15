---
description: Cette rubrique décrit les bibliothèques et leurs avantages pour les utilisateurs et les développeurs.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: À propos des bibliothèques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554857"
---
# <a name="about-libraries"></a><span data-ttu-id="4d464-103">À propos des bibliothèques</span><span class="sxs-lookup"><span data-stu-id="4d464-103">About Libraries</span></span>

<span data-ttu-id="4d464-104">Cette rubrique décrit les bibliothèques et leurs avantages pour les utilisateurs et les développeurs.</span><span class="sxs-lookup"><span data-stu-id="4d464-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="4d464-105">Les bibliothèques sont des collections de dossiers définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4d464-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="4d464-106">Une bibliothèque effectue le suivi de l’emplacement de stockage physique de chaque dossier, ce qui allège l’utilisateur et le logiciel de cette tâche.</span><span class="sxs-lookup"><span data-stu-id="4d464-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="4d464-107">Les utilisateurs peuvent regrouper des dossiers connexes dans une bibliothèque, même si ces dossiers sont stockés sur des disques durs différents ou sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="4d464-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="4d464-108">Dans une bibliothèque, les dossiers et fichiers apparaissent à l’utilisateur sous la forme d’une collection unique et, à l’aide de l’API de bibliothèque de l’interpréteur de commandes, le contenu de la bibliothèque peut également sembler se trouver à un emplacement unique pour un programme.</span><span class="sxs-lookup"><span data-stu-id="4d464-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="4d464-109">Dans une bibliothèque, le contenu, tel que les documents, les photos, les vidéos ou la musique d’un utilisateur, peut être trié et affiché lorsque l’utilisateur le souhaite et pas simplement comme le système de fichiers le requiert.</span><span class="sxs-lookup"><span data-stu-id="4d464-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="4d464-110">Par exemple, les utilisateurs peuvent organiser le contenu d’une bibliothèque à l’aide des propriétés des éléments de la bibliothèque afin que les éléments associés soient triés ensemble, même s’ils sont stockés dans des dossiers différents.</span><span class="sxs-lookup"><span data-stu-id="4d464-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![capture d’écran de l’interface utilisateur des bibliothèques](images/libraries-whatare.png)

<span data-ttu-id="4d464-112">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="4d464-112">In this topic:</span></span>

-   [<span data-ttu-id="4d464-113">Avantages de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d464-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="4d464-114">Avantages de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4d464-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="4d464-115">Avantages pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="4d464-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="4d464-116">Gestion des dossiers dans les bibliothèques</span><span class="sxs-lookup"><span data-stu-id="4d464-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="4d464-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d464-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="4d464-118">Avantages de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d464-118">Library Benefits</span></span>

<span data-ttu-id="4d464-119">Cette section décrit certains des avantages des bibliothèques du point de vue de l’utilisateur final et du point de vue du développeur de programme.</span><span class="sxs-lookup"><span data-stu-id="4d464-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="4d464-120">Avantages de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4d464-120">User Benefits</span></span>

<span data-ttu-id="4d464-121">L’ajout de la prise en charge de bibliothèque à votre programme offre les avantages suivants à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="4d464-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="4d464-122">**Les bibliothèques fournissent une interface utilisateur cohérente dans Windows 7**</span><span class="sxs-lookup"><span data-stu-id="4d464-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="4d464-123">Les boîtes de dialogue de fichier courantes prennent en charge les bibliothèques et fournissent la même expérience utilisateur que l’Explorateur Windows dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4d464-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="4d464-124">Les bibliothèques de prise en charge dans votre programme vous aideront à fournir une interaction plus transparente pour l’utilisateur lors de l’utilisation de votre programme dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4d464-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="4d464-125">**Les utilisateurs décident de l’emplacement de stockage du contenu**</span><span class="sxs-lookup"><span data-stu-id="4d464-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="4d464-126">Les bibliothèques permettent aux utilisateurs de contrôler l’emplacement de stockage de leur contenu.</span><span class="sxs-lookup"><span data-stu-id="4d464-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="4d464-127">En même temps, les bibliothèques fournissent des valeurs par défaut raisonnables pour les utilisateurs qui ne souhaitent pas gérer ce niveau de détail sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4d464-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="4d464-128">Les utilisateurs décident de la quantité de contrôle qu’ils veulent consacrer à l’emplacement et à la façon dont le contenu est stocké, et la bibliothèque fonctionne correctement dans les deux cas.</span><span class="sxs-lookup"><span data-stu-id="4d464-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="4d464-129">Avantages pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="4d464-129">Developer Benefits</span></span>

<span data-ttu-id="4d464-130">Vous pouvez utiliser des bibliothèques dans votre programme pour fournir une interface utilisateur plus flexible et plus pratique sans avoir à ajouter beaucoup de code de programme complexe.</span><span class="sxs-lookup"><span data-stu-id="4d464-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="4d464-131">Voici quelques-uns des avantages de l’ajout de la prise en charge de bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="4d464-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="4d464-132">**Les bibliothèques prennent en charge l’accès à la bibliothèque et au système de fichiers**</span><span class="sxs-lookup"><span data-stu-id="4d464-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="4d464-133">À l’aide de l’API de la [**bibliothèque Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), les programmes peuvent assurer la prise en charge de la bibliothèque pour l’utilisateur tout en réduisant la complexité du code de gestion des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="4d464-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="4d464-134">Si votre programme utilise déjà l’API du système de fichiers, vous pouvez conserver autant de code existant que vous le souhaitez, tout en fournissant la prise en charge de la bibliothèque à l’utilisateur en obtenant les informations de système de fichiers nécessaires à partir de l’API de la bibliothèque de l' **interpréteur** de commandes.</span><span class="sxs-lookup"><span data-stu-id="4d464-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="4d464-135">**Notification de modification plus simple**</span><span class="sxs-lookup"><span data-stu-id="4d464-135">**Simpler change notification**</span></span>

    <span data-ttu-id="4d464-136">Le système de fichiers et l’API de l’interpréteur de commandes peuvent notifier votre programme lorsque le contenu d’un dossier ou d’une bibliothèque contrôlé change.</span><span class="sxs-lookup"><span data-stu-id="4d464-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="4d464-137">Toutefois, à l’aide de l’API Shell, vous pouvez surveiller tous les dossiers de la bibliothèque avec une seule notification, même si le dossier de la bibliothèque peut être stocké sur des lecteurs différents, voire sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="4d464-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="4d464-138">**Les bibliothèques utilisent les propriétés de fichier**</span><span class="sxs-lookup"><span data-stu-id="4d464-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="4d464-139">Les programmes peuvent utiliser les propriétés de fichier pour contrôler les fichiers qui sont affichés pendant les opérations d’ouverture et d’enregistrement qui utilisent les boîtes de dialogue de fichier courantes.</span><span class="sxs-lookup"><span data-stu-id="4d464-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="4d464-140">Les programmes peuvent également avoir accès aux propriétés de fichier à l’aide des interfaces [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="4d464-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="4d464-141">Les boîtes de dialogue de fichier courantes peuvent également être configurées pour permettre aux utilisateurs de mettre à jour les propriétés associées à leur contenu.</span><span class="sxs-lookup"><span data-stu-id="4d464-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="4d464-142">**Les programmes peuvent créer des bibliothèques dédiées**</span><span class="sxs-lookup"><span data-stu-id="4d464-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="4d464-143">Une nouvelle bibliothèque peut être créée lorsqu’une bibliothèque utilisateur existante ne répond pas aux besoins du programme, par exemple, si un programme crée un nouveau type de contenu utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4d464-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="4d464-144">La nouvelle bibliothèque peut être configurée avec une icône unique qui représente son contenu et facilite l’identification de la bibliothèque dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4d464-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="4d464-145">Gestion des dossiers dans les bibliothèques</span><span class="sxs-lookup"><span data-stu-id="4d464-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="4d464-146">Les utilisateurs peuvent organiser leurs bibliothèques en ajoutant, en déplaçant ou en supprimant des dossiers dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4d464-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="4d464-147">Toutefois, tous les dossiers ne prennent pas en charge toutes les fonctionnalités qu’une bibliothèque peut fournir.</span><span class="sxs-lookup"><span data-stu-id="4d464-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="4d464-148">De nombreuses fonctionnalités de bibliothèque requièrent un accès rapide aux différentes propriétés du dossier et à son contenu qui sont uniquement disponibles par le biais de la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="4d464-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="4d464-149">Pour fournir une fonctionnalité de bibliothèque complète, un dossier doit pouvoir être indexé par la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="4d464-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="4d464-150">Une bibliothèque n’autorise pas un utilisateur à ajouter des dossiers qui ne fournissent pas toutes les fonctionnalités de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4d464-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="4d464-151">Toutefois, l’API de la [**bibliothèque de shells**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) peut ajouter de tels dossiers.</span><span class="sxs-lookup"><span data-stu-id="4d464-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="4d464-152">Si une bibliothèque contient un dossier qui ne prend pas en charge la fonctionnalité de bibliothèque complète, la bibliothèque fonctionne en mode sans échec et fournit une fonctionnalité limitée.</span><span class="sxs-lookup"><span data-stu-id="4d464-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="4d464-153">Le tableau suivant décrit les dossiers qui prennent en charge la fonctionnalité de bibliothèque complète et ceux qui ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="4d464-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="4d464-154">Types de dossiers qui prennent en charge la fonctionnalité de bibliothèque complète</span><span class="sxs-lookup"><span data-stu-id="4d464-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="4d464-155">Types de dossiers qui ne prennent pas en charge la fonctionnalité de bibliothèque complète</span><span class="sxs-lookup"><span data-stu-id="4d464-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d464-156">Disques durs NTFS et NTFS fixes et externes.</span><span class="sxs-lookup"><span data-stu-id="4d464-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="4d464-157">Lecteurs amovibles tels que les lecteurs flash USB ou les cartes mémoire Secure Digital (SD).</span><span class="sxs-lookup"><span data-stu-id="4d464-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="4d464-158">Partages de fichiers indexés par Windows Search, tels que les serveurs départementaux, Windows 7 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4d464-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="4d464-159">Support amovible, tel qu’un CD-ROM ou un DVD.</span><span class="sxs-lookup"><span data-stu-id="4d464-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="4d464-160">Les partages de fichiers qui sont disponibles hors connexion, tels qu’un dossier **Mes documents** Redirigé ou un cache Client-Side.</span><span class="sxs-lookup"><span data-stu-id="4d464-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="4d464-161">Partages réseau qui ne sont pas disponibles hors connexion ni indexés à distance, tels que les lecteurs NAS.</span><span class="sxs-lookup"><span data-stu-id="4d464-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="4d464-162">D’autres sources de données telles que Microsoft SharePoint, Microsoft Exchange et Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="4d464-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="4d464-163">L’illustration suivante montre l’affichage limité du contenu de la bibliothèque en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="4d464-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![ouvrir la boîte de dialogue lorsque les bibliothèques sont en mode sans échec](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="4d464-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d464-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d464-166">À propos des bibliothèques</span><span class="sxs-lookup"><span data-stu-id="4d464-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="4d464-167">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="4d464-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="4d464-168">Liens de Shell</span><span class="sxs-lookup"><span data-stu-id="4d464-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="4d464-169">Dossiers connus</span><span class="sxs-lookup"><span data-stu-id="4d464-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="4d464-170">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d464-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
