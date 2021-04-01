---
description: Les associations de fichiers définissent la façon dont l’interpréteur de commandes traite un type de fichier sur le système.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Fonctionnement des associations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202799"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="dff17-103">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-103">How File Associations Work</span></span>

<span data-ttu-id="dff17-104">Les associations de fichiers définissent la façon dont l’interpréteur de commandes traite un [type de fichier](fa-file-types.md) sur le système.</span><span class="sxs-lookup"><span data-stu-id="dff17-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="dff17-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="dff17-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="dff17-106">À propos des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="dff17-107">Lorsque vous devez implémenter ou modifier des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="dff17-108">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="dff17-109">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="dff17-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="dff17-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dff17-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="dff17-111">À propos des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-111">About File Associations</span></span>

<span data-ttu-id="dff17-112">Les associations de fichiers contrôlent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="dff17-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="dff17-113">L’application qui démarre lorsqu’un utilisateur double-clique sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="dff17-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="dff17-114">L’icône qui s’affiche pour un fichier par défaut.</span><span class="sxs-lookup"><span data-stu-id="dff17-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="dff17-115">Mode d’affichage du type de fichier dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="dff17-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="dff17-116">Les commandes qui s’affichent dans le menu contextuel d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="dff17-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="dff17-117">Autres fonctionnalités de l’interface utilisateur, telles que les info-bulles, les informations de vignette et le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="dff17-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="dff17-118">Les développeurs d’applications peuvent utiliser des associations de fichiers pour contrôler la façon dont l’interpréteur de commandes traite les types de fichiers personnalisés, ou pour associer une application à des types de fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="dff17-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="dff17-119">Par exemple, lorsqu’une application est installée, l’application peut vérifier la présence d’associations de fichiers existantes et créer ou remplacer ces associations de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dff17-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="dff17-120">Les utilisateurs peuvent contrôler certains aspects des associations de fichiers pour personnaliser la façon dont l’interpréteur de commandes traite un type de fichier à l’aide de l’interface utilisateur **ouverte** ou de la modification du Registre.</span><span class="sxs-lookup"><span data-stu-id="dff17-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="dff17-121">Dans la fenêtre de l’Explorateur Windows présentée dans la capture d’écran ci-dessous, l’interpréteur de commandes affiche différentes icônes pour chaque fichier, en fonction de l’icône associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="dff17-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="dff17-122">Si l’utilisateur double-clique sur l' **image bitmap** de l’exemple de fichier, l’interpréteur de commandes lance Paint et l’utilise pour ouvrir le fichier, car sur ce système, Paint est associé aux fichiers. bmp.</span><span class="sxs-lookup"><span data-stu-id="dff17-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="dff17-123">Les utilisateurs peuvent contrôler ces actions à l’aide d’associations de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dff17-123">People can control these actions using file associations.</span></span>

![illustration du fonctionnement des associations de fichiers dans la pratique](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="dff17-125">Lorsque vous devez implémenter ou modifier des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="dff17-126">Les applications peuvent utiliser des fichiers à diverses fins : certains fichiers sont utilisés exclusivement par l’application et ne sont généralement pas accessibles aux utilisateurs, tandis que d’autres fichiers sont créés par l’utilisateur et sont souvent ouverts, recherchés et consultés à partir de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="dff17-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="dff17-127">À moins que votre type de fichier personnalisé ne soit utilisé exclusivement par l’application, vous devez implémenter des associations de fichiers pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="dff17-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="dff17-128">En règle générale, implémentez des associations de fichiers pour votre type de fichier personnalisé si vous vous attendez à ce que l’utilisateur interagisse directement avec ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="dff17-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="dff17-129">Cela comprend l’utilisation de l’interpréteur de commandes pour parcourir et ouvrir les fichiers, Rechercher le contenu ou les propriétés des fichiers et afficher un aperçu des fichiers.</span><span class="sxs-lookup"><span data-stu-id="dff17-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="dff17-130">Si votre application gère un type de fichier existant, ne modifiez pas l’Association de fichiers, sauf si vous souhaitez modifier la façon dont l’interpréteur de commandes gère tous les fichiers de ce type.</span><span class="sxs-lookup"><span data-stu-id="dff17-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="dff17-131">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-131">How File Associations Work</span></span>

<span data-ttu-id="dff17-132">Les fichiers sont exposés dans le shell en tant qu’éléments de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="dff17-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="dff17-133">Pour contrôler les associations de fichiers, les développeurs d’applications peuvent inscrire un mappage entre le type de fichier et les gestionnaires (objets COM qui fournissent des fonctionnalités pour les éléments de Shell du type de fichier).</span><span class="sxs-lookup"><span data-stu-id="dff17-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="dff17-134">Lorsque l’interpréteur de commandes doit interroger les associations de fichiers d’un type de fichier, il crée un tableau de clés de registre contenant les associations pour le type de fichier et vérifie ces clés pour les associations de fichiers appropriées à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dff17-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dff17-135">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="dff17-135">Additional Resources</span></span>

-   <span data-ttu-id="dff17-136">Pour obtenir des informations conceptuelles sur les associations de fichiers, consultez [vue d’ensemble des verbes et des associations de fichiers](fa-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="dff17-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dff17-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dff17-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dff17-138">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="dff17-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="dff17-139">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="dff17-140">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="dff17-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="dff17-141">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="dff17-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="dff17-142">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="dff17-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="dff17-143">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="dff17-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="dff17-144">Types perçus</span><span class="sxs-lookup"><span data-stu-id="dff17-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="dff17-145">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="dff17-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



