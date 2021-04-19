---
title: Comment développer une application OEM qui utilise un fichier personnalisé
description: Découvrez comment développer une application qui utilise un fichier personnalisé pour transmettre des informations de l’OEM à l’application.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "106511676"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="03030-103">Comment développer une application OEM qui utilise un fichier personnalisé</span><span class="sxs-lookup"><span data-stu-id="03030-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="03030-104">Pour plus d’informations sur la création et l’utilisation de fichiers de données personnalisés, consultez [options de maintenance de package d’application DISM (. AppX ou. appxbundle) Command-Line options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span><span class="sxs-lookup"><span data-stu-id="03030-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="03030-105">Découvrez comment développer une application qui utilise un fichier personnalisé pour transmettre des informations de l’OEM à l’application.</span><span class="sxs-lookup"><span data-stu-id="03030-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="03030-106">Pour les applications que vous créez pour le déploiement OEM, vous pouvez utiliser un fichier personnalisé pour transmettre les informations du fabricant OEM aux applications.</span><span class="sxs-lookup"><span data-stu-id="03030-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="03030-107">Pour transmettre des informations OEM à une application, vous créez un fichier. Data personnalisé dans le dossier microsoft.sysTEM. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="03030-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="03030-108">Ce nom de fichier est spécial pour le système d’exploitation et est automatiquement transféré au cours des mises à jour du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="03030-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="03030-109">Les fabricants d’ordinateurs OEM peuvent utiliser ce fichier pour transmettre des identificateurs personnalisés, afin que les applications sachent quand les OEM les ont déployées.</span><span class="sxs-lookup"><span data-stu-id="03030-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="03030-110">Vous ne pouvez avoir qu’un seul fichier. Data personnalisé par application.</span><span class="sxs-lookup"><span data-stu-id="03030-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="03030-111">Les applications doivent être en mesure de rechercher et de lire ce fichier correctement.</span><span class="sxs-lookup"><span data-stu-id="03030-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="03030-112">Les développeurs traitent le fichier comme des données non fiables.</span><span class="sxs-lookup"><span data-stu-id="03030-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="03030-113">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="03030-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="03030-114">Technologies</span><span class="sxs-lookup"><span data-stu-id="03030-114">Technologies</span></span>

-   [<span data-ttu-id="03030-115">Démarrage rapide : interroger les informations du manifeste du package d’application</span><span class="sxs-lookup"><span data-stu-id="03030-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="03030-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="03030-116">Prerequisites</span></span>

-   <span data-ttu-id="03030-117">Vous avez besoin de l’outil [gestion et maintenance des images de déploiement (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) pour ajouter le package d’application avec le fichier de données personnalisé.</span><span class="sxs-lookup"><span data-stu-id="03030-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="03030-118">Instructions</span><span class="sxs-lookup"><span data-stu-id="03030-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="03030-119">Étape 1 : créer un fichier personnalisé et l’ajouter au dossier de métadonnées du package</span><span class="sxs-lookup"><span data-stu-id="03030-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="03030-120">Vous pouvez concevoir votre application pour qu’elle utilise le format de votre choix pour les données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="03030-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="03030-121">Par exemple, vous pouvez utiliser XML, un fichier texte ou un autre type de fichier pour organiser vos données.</span><span class="sxs-lookup"><span data-stu-id="03030-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="03030-122">Nous vous recommandons de réfléchir à la façon dont vous pouvez tester et valider le fichier.</span><span class="sxs-lookup"><span data-stu-id="03030-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="03030-123">Par exemple, vous pouvez créer un schéma XML pour valider un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="03030-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="03030-124">Vous pouvez spécifier n’importe quel type de fichier avec n’importe quel nom de fichier pour les données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="03030-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="03030-125">Lorsque vous ajoutez le package d’application avec le fichier de données personnalisé à l’aide de l’outil [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , DISM renomme le fichier personnalisé en Custom. Data et enregistre le fichier dans le dossier microsoft.sysTEM. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="03030-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="03030-126">Le fichier de données personnalisé ne peut pas être modifié par l’application.</span><span class="sxs-lookup"><span data-stu-id="03030-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="03030-127">Il s’agit d’une ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03030-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="03030-128">Étape 2 : accéder au fichier de données personnalisé pour une application</span><span class="sxs-lookup"><span data-stu-id="03030-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="03030-129">Vous pouvez accéder au fichier. Data personnalisé d’une application à partir de votre code à l’aide des API Windows pour obtenir des informations sur le package actuel.</span><span class="sxs-lookup"><span data-stu-id="03030-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="03030-130">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="03030-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="03030-131">Pour plus d’informations sur le développement avec la propriété [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , consultez [démarrage rapide : interroger les informations du manifeste du package d’application](how-to-query-package-identity-information.md).</span><span class="sxs-lookup"><span data-stu-id="03030-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="03030-132">Pour plus d’informations sur l’accès au fichier. Data personnalisé via [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) et l’utilisation d’objets [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , consultez [accès aux données et aux fichiers](/previous-versions/windows/apps/hh464959(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="03030-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03030-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03030-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03030-134">Démarrage rapide : interroger les informations du manifeste du package d’application</span><span class="sxs-lookup"><span data-stu-id="03030-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 