---
description: Cette rubrique explique comment créer une application MUI standard.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localisation des ressources et génération de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524929"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="78c14-103">Localisation des ressources et génération de l’application</span><span class="sxs-lookup"><span data-stu-id="78c14-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="78c14-104">Cette rubrique explique comment créer une application MUI standard.</span><span class="sxs-lookup"><span data-stu-id="78c14-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="78c14-105">Il est supposé que vous utilisez Microsoft Visual Studio pour le codage et Microsoft Visual Studio ou la ligne de commande Visual Studio pour la génération.</span><span class="sxs-lookup"><span data-stu-id="78c14-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="78c14-106">Vous êtes supposé utiliser un fichier solution. sln pour votre application et prendre en charge un fichier Resource. h pour refléter le fichier de ressources de la langue de base.</span><span class="sxs-lookup"><span data-stu-id="78c14-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="78c14-107">Si vous utilisez la ligne de commande Visual Studio pour la génération, vous allez utiliser la commande **VCBUILD** pour générer le fichier solution.</span><span class="sxs-lookup"><span data-stu-id="78c14-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="78c14-108">Les fichiers d’application sont générés séparément pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="78c14-108">Application files are built separately for each language.</span></span> <span data-ttu-id="78c14-109">Chaque Build crée des fichiers. exe. exe et des fichiers. exe. mui de langue identique neutres.</span><span class="sxs-lookup"><span data-stu-id="78c14-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="78c14-110">En outre, plusieurs autres fichiers sont copiés dans les dossiers de version appropriés.</span><span class="sxs-lookup"><span data-stu-id="78c14-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="78c14-111">La génération de l’application dépend du type de ressources et du type de localisation que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="78c14-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="78c14-112">Pour la localisation pré-build, vous disposez d’une copie du fichier de langue de base localisée pour chaque langue prise en charge.</span><span class="sxs-lookup"><span data-stu-id="78c14-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="78c14-113">Pour la localisation après génération, vous pouvez copier le fichier. mui résultant de la génération du module exécutable et du module de ressources, et fournir les copies aux localiseurs.</span><span class="sxs-lookup"><span data-stu-id="78c14-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="78c14-114">La procédure suivante suppose des ressources Win32 PE avec un projet Visual Studio généré pour chaque langage.</span><span class="sxs-lookup"><span data-stu-id="78c14-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="78c14-115">Les ressources linguistiques de base sont fournies dans un fichier. RC et chargées à l’aide d’un module DLL.</span><span class="sxs-lookup"><span data-stu-id="78c14-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="78c14-116">Vous pouvez répéter la procédure en fonction des besoins pour générer toutes les langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="78c14-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="78c14-117">**Pour générer l’application**</span><span class="sxs-lookup"><span data-stu-id="78c14-117">**To build the application**</span></span>

1.  <span data-ttu-id="78c14-118">Configurez un projet Visual Studio pour la langue de base.</span><span class="sxs-lookup"><span data-stu-id="78c14-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="78c14-119">Si vous souhaitez utiliser un fichier de configuration de ressources avec les outils de ressources, définissez-en un comme décrit dans [préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="78c14-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="78c14-120">Définissez les paramètres requis par l’utilitaire du compilateur RC dans les pages de propriétés du projet sous **Propriétés de configuration → ressources → ligne de commande → Options supplémentaires**.</span><span class="sxs-lookup"><span data-stu-id="78c14-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="78c14-121">Exécutez le compilateur RC.</span><span class="sxs-lookup"><span data-stu-id="78c14-121">Run RC Compiler.</span></span> <span data-ttu-id="78c14-122">L’utilitaire compile et fractionne les ressources non localisables et localisables en deux fichiers objets différents, à l’aide des données de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="78c14-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="78c14-123">Dans cette étape, les ressources indépendantes du langage sont liées à un fichier LN.</span><span class="sxs-lookup"><span data-stu-id="78c14-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="78c14-124">Pour plus d’informations, consultez la description de l’utilitaire dans les [utilitaires de ressource](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="78c14-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="78c14-125">Pour lier les ressources spécifiques à une langue dans un fichier. mui spécifique à une langue, définissez un événement après génération pour le projet dans les pages de propriétés sous **Propriétés de configuration → événements de build → événement après génération → ligne de commande**.</span><span class="sxs-lookup"><span data-stu-id="78c14-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="78c14-126">Définissez un événement après génération pour appliquer la valeur de somme de contrôle du fichier LN au fichier. mui pour la langue.</span><span class="sxs-lookup"><span data-stu-id="78c14-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="78c14-127">Vous pouvez utiliser l’utilitaire MUIRCT pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="78c14-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="78c14-128">Pour plus d’informations, consultez la description de l’utilitaire dans les [utilitaires de ressource](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="78c14-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="78c14-129">Utilisez la ligne de commande de l’événement après génération pour ajouter des commandes permettant de copier les fichiers dans la structure de dossiers de la version appropriée.</span><span class="sxs-lookup"><span data-stu-id="78c14-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78c14-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78c14-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78c14-131">Utilisation de l’interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="78c14-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="78c14-132">Préparation d’un fichier de configuration de ressource</span><span class="sxs-lookup"><span data-stu-id="78c14-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="78c14-133">Utilitaires de ressource</span><span class="sxs-lookup"><span data-stu-id="78c14-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



