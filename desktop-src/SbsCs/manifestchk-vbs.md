---
description: Le Manifestchk.vbs de fichier VBScript est un outil de validation fourni dans le kit de développement logiciel (SDK) Microsoft Windows qui valide les fichiers de manifeste de l’application et de l’assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393595"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="e79c3-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="e79c3-103">Manifestchk.vbs</span></span>

<span data-ttu-id="e79c3-104">Le Manifestchk.vbs de fichier VBScript est un outil de validation fourni dans le kit de développement logiciel (SDK) Microsoft Windows qui valide les fichiers de manifeste de l’application et de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e79c3-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="e79c3-105">L’exécution de cet exemple nécessite Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="e79c3-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="e79c3-106">Pour plus d’informations sur Windows Script Host, consultez la section Windows Script Host de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="e79c3-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="e79c3-107">Windows Script Host est en fait deux hôtes.</span><span class="sxs-lookup"><span data-stu-id="e79c3-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="e79c3-108">CScript.exe est la version qui vous permet d’exécuter des scripts à partir de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="e79c3-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="e79c3-109">CScript.exe fournit des commutateurs de ligne de commande pour définir les propriétés de script.</span><span class="sxs-lookup"><span data-stu-id="e79c3-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="e79c3-110">Le format de ligne de commande est le suivant :</span><span class="sxs-lookup"><span data-stu-id="e79c3-110">The command-line format is the following:</span></span>

<span data-ttu-id="e79c3-111">**Cscript//nologo manifestchk.vbs/s :** *\[ lecteur : \] \[ chemin d’accès \] schemafilename* **/m :** *\[ lecteur : \] \[ chemin \] ManifestFileName* **\[ /q \] /t :** *option*</span><span class="sxs-lookup"><span data-stu-id="e79c3-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="e79c3-112">Les indicateurs définis pour Manifestchk.vbs sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e79c3-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="e79c3-113">Indicateur</span><span class="sxs-lookup"><span data-stu-id="e79c3-113">Flag</span></span> | <span data-ttu-id="e79c3-114">Description</span><span class="sxs-lookup"><span data-stu-id="e79c3-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e79c3-115">/s</span><span class="sxs-lookup"><span data-stu-id="e79c3-115">/s</span></span>   | <span data-ttu-id="e79c3-116">Spécifie le nom du fichier de schéma du manifeste pour la validation des manifestes.</span><span class="sxs-lookup"><span data-stu-id="e79c3-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="e79c3-117">Consultez le schéma dans le [schéma de fichier manifeste](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e79c3-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e79c3-118">/m</span><span class="sxs-lookup"><span data-stu-id="e79c3-118">/m</span></span>   | <span data-ttu-id="e79c3-119">Spécifie le nom du fichier manifeste à valider.</span><span class="sxs-lookup"><span data-stu-id="e79c3-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e79c3-120">/q</span><span class="sxs-lookup"><span data-stu-id="e79c3-120">/q</span></span>   | <span data-ttu-id="e79c3-121">Supprime toutes les sorties de la console.</span><span class="sxs-lookup"><span data-stu-id="e79c3-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e79c3-122">/t</span><span class="sxs-lookup"><span data-stu-id="e79c3-122">/t</span></span>   | <span data-ttu-id="e79c3-123">Spécifie le type de fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="e79c3-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="e79c3-124">Les valeurs valides sont : AM valide le [schéma de fichier manifeste](manifest-file-schema.md) d’un manifeste d' [assembly](assembly-manifests.md) ou d’un [manifeste d’application](application-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="e79c3-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="e79c3-125">Le PC valide le [schéma du fichier de configuration](publisher-configuration-file-schema.md) du serveur de publication d’un fichier de configuration d' [éditeur](publisher-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="e79c3-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="e79c3-126">AC validez le schéma de fichier de configuration d’application d’un [fichier de configuration d’application](application-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="e79c3-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="e79c3-127">Si l’indicateur/q n’est pas spécifié, Manifestchk.vbs affiche des informations détaillées sur la première erreur rencontrée dans le fichier et affiche un message indiquant si le processus de validation a réussi ou non.</span><span class="sxs-lookup"><span data-stu-id="e79c3-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="e79c3-128">Cet utilitaire vérifie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e79c3-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="e79c3-129">Une ligne de commande valide.</span><span class="sxs-lookup"><span data-stu-id="e79c3-129">A valid command line.</span></span>
-   <span data-ttu-id="e79c3-130">Cette version de MSXML 3 est installée.</span><span class="sxs-lookup"><span data-stu-id="e79c3-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="e79c3-131">Que le manifeste utilise du XML bien formé.</span><span class="sxs-lookup"><span data-stu-id="e79c3-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="e79c3-132">Que le manifeste accepte le schéma fourni.</span><span class="sxs-lookup"><span data-stu-id="e79c3-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="e79c3-133">Notez que Manifestchk.vbs vérifie le fichier manifeste en fonction de ce qui est spécifié dans le schéma fourni.</span><span class="sxs-lookup"><span data-stu-id="e79c3-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="e79c3-134">Pour obtenir un exemple de schéma de manifeste, consultez [schéma de fichier manifeste](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e79c3-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="e79c3-135">Cscript.exe retourne la valeur 0 si le processus de validation a réussi et 1 s’il n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e79c3-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="e79c3-136">Elle retourne 2 s’il y a une erreur dans un argument de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e79c3-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e79c3-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e79c3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e79c3-138">Outils de développement d’assembly côte à côte</span><span class="sxs-lookup"><span data-stu-id="e79c3-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




