---
description: Les modules de fusion fournissent une méthode standard pour vous permettre de fournir des composants de Windows Installer partagés et une logique de configuration aux applications.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Utilisation de l’automatisation pour fusionner un module de fusion dans une base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514245"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="4a1dc-103">Utilisation de l’automatisation pour fusionner un module de fusion dans une base de données</span><span class="sxs-lookup"><span data-stu-id="4a1dc-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="4a1dc-104">Les [modules de fusion](merge-modules.md) fournissent une méthode standard pour vous permettre de fournir des [*composants*](c-gly.md)de Windows Installer partagés et une logique de configuration aux applications.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="4a1dc-105">Les modules de fusion doivent être fusionnés dans un package d’installation à l’aide d’un outil de fusion.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="4a1dc-106">La meilleure pratique consiste à obtenir un outil de fusion distribué librement, ou à acheter l’un des outils de fusion disponibles auprès des éditeurs de logiciels indépendants, par exemple, vous pouvez utiliser [Mergemod.dll](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="4a1dc-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="4a1dc-107">La procédure suivante montre comment fusionner un module de fusion dans une base de données Windows Installer à l’aide de l' [automatisation des modules de fusion](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="4a1dc-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="4a1dc-108">**Pour fusionner un module dans une base de données**</span><span class="sxs-lookup"><span data-stu-id="4a1dc-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="4a1dc-109">Ouvrez un fichier journal à l’aide de la méthode [**OpenLog**](merge-openlog.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="4a1dc-110">Cette étape est requise uniquement si vous devez créer un fichier journal ou ajouter un fichier journal existant pour le processus de fusion.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="4a1dc-111">Ouvrez la base de données d’installation [. msi](windows-installer-file-extensions.md) à l’aide de la méthode [**OpenDatabase**](merge-opendatabase.md) de l' [**objet Merge**](merge-object.md).</span><span class="sxs-lookup"><span data-stu-id="4a1dc-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="4a1dc-112">Cette étape est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-112">This step is required.</span></span>

    <span data-ttu-id="4a1dc-113">La base de données que vous ouvrez est celle pour laquelle vous souhaitez recevoir le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="4a1dc-114">Ouvrez le module de fusion [. msm](windows-installer-file-extensions.md) à l’aide de la méthode [**OpenModule**](merge-openmodule.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="4a1dc-115">Cette étape est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-115">This step is required.</span></span>

    <span data-ttu-id="4a1dc-116">Il s’agit du module de fusion qui est fusionné dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="4a1dc-117">Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="4a1dc-118">Fusionnez le module dans la base de données d’installation en appelant la méthode [**Merge**](merge-object.md) ou la méthode [**MergeEx**](merge-mergeex.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="4a1dc-119">Cette étape est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-119">This step is required.</span></span>

    <span data-ttu-id="4a1dc-120">La méthode [**Merge**](merge-object.md) ou la méthode [**MergeEx**](merge-mergeex.md) ne peut être appelée qu’une seule fois pour fusionner une combinaison spécifique de fichiers [. msi](windows-installer-file-extensions.md) et. msm.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="4a1dc-121">La méthode [**MergeEx**](merge-mergeex.md) est uniquement disponible dans [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure, et uniquement lors de l’utilisation de l’interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="4a1dc-122">Récupérez la propriété [**Errors**](merge-errors.md) et examinez la collection d’objets d' [**erreur**](error-object.md) qu’elle renvoie pour les conflits de fusion ou d’autres erreurs.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="4a1dc-123">Vous devez résoudre toutes les erreurs.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-123">You must resolve any errors.</span></span>

    <span data-ttu-id="4a1dc-124">La récupération n’est pas destructrice et plusieurs instances de la collection d’erreurs peuvent être récupérées en lisant de manière répétée la propriété [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="4a1dc-125">Associez les composants du module de fusion aux fonctionnalités à l’aide de la méthode [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="4a1dc-126">Cette étape est requise uniquement si vous disposez de fonctionnalités existantes et que vous souhaitez ajouter des fonctionnalités à fusionner dans la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="4a1dc-127">Une fonctionnalité doit exister avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="4a1dc-128">Pour plus d’informations, consultez [connexion d’un module de fusion à plusieurs fonctionnalités](connecting-a-merge-module-to-multiple-features.md).</span><span class="sxs-lookup"><span data-stu-id="4a1dc-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="4a1dc-129">Si nécessaire, extrayez les fichiers sources du module en exécutant une ou plusieurs des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a1dc-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="4a1dc-130">Utilisez [**ExtractFiles**](merge-extractfiles.md) ou [**ExtractFilesEx**](merge-extractfilesex.md) pour extraire des fichiers d’un fichier. cab incorporé, puis copiez-les dans un répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="4a1dc-131">[**ExtractFilesEx**](merge-extractfilesex.md) requiert [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="4a1dc-132">Utilisez [**ExtractCAB**](merge-extractcab.md) pour extraire les fichiers d’un fichier. cab incorporé, puis enregistrez-les dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="4a1dc-133">Utilisez [**CreateSourceImage**](merge-createsourceimage.md) pour extraire les fichiers d’un module, puis, après la fusion, copiez-les dans une image source sur le disque.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="4a1dc-134">[**CreateSourceImage**](merge-createsourceimage.md) est disponible uniquement dans [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="4a1dc-135">Fermez le module de fusion ouvert en cours à l’aide de la méthode [**CloseModule**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="4a1dc-136">Cette étape est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-136">This step is required.</span></span>

9.  <span data-ttu-id="4a1dc-137">Fermez la base de données d’installation ouverte à l’aide de la méthode [**FermerBase**](merge-closedatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="4a1dc-138">Cette étape est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-138">This step is required.</span></span>

    <span data-ttu-id="4a1dc-139">La fermeture d’une base de données efface toutes les informations de dépendance, mais n’affecte pas les erreurs qui ne sont pas récupérées.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="4a1dc-140">Fermez le fichier journal actuel à l’aide de la méthode [**CloseLog**](merge-closelog.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1dc-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="4a1dc-141">Cette étape est requise si vous disposez d’un fichier journal ouvert.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="4a1dc-142">Une fois le module fusionné dans la base de données à l’aide de [Mergemod.dll](merge-module-automation.md), la [table de supports](media-table.md) doit être mise à jour pour décrire la disposition souhaitée de l’image source.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="4a1dc-143">Le processus de fusion fourni par Mergemod.dll ne met pas à jour la table multimédia, car l’utilisateur du module de fusion peut sélectionner différentes méthodes pour la disposition de l’image source.</span><span class="sxs-lookup"><span data-stu-id="4a1dc-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a1dc-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a1dc-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a1dc-145">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="4a1dc-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



