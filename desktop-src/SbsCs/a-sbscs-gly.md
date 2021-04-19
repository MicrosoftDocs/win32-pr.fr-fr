---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518668"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="d263c-103">A (applications isolées et assemblys côte à côte)</span><span class="sxs-lookup"><span data-stu-id="d263c-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="d263c-104">A B C [D](d-sbscs-gly.md) e F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="d263c-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d263c-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexte d’activation**</span><span class="sxs-lookup"><span data-stu-id="d263c-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="d263c-106">Structure de données en mémoire.</span><span class="sxs-lookup"><span data-stu-id="d263c-106">A data structure in memory.</span></span> <span data-ttu-id="d263c-107">Chaque section de cette structure contient des métadonnées pour les fonctions d’API de prise en charge côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d263c-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="d263c-108">Par exemple, une section peut contenir des données de redirection de DLL, qui sont utilisées par le chargeur de DLL, et une autre peut comporter des données de serveur COM.</span><span class="sxs-lookup"><span data-stu-id="d263c-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="d263c-109">Ces données peuvent être utilisées pour rediriger le chargement d’une DLL vers une version spécifique, la création d’un objet COM ou la création d’une fenêtre avec une version la plus compatible pour l’application.</span><span class="sxs-lookup"><span data-stu-id="d263c-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="d263c-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuration de l’application**</span><span class="sxs-lookup"><span data-stu-id="d263c-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="d263c-111">Noms et versions des assemblys côte à côte requis pour exécuter une application.</span><span class="sxs-lookup"><span data-stu-id="d263c-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="d263c-112">Quand une application est déployée avec un manifeste, les dépendances sur des versions spécifiques des assemblys côte à côte partagés sont définies explicitement.</span><span class="sxs-lookup"><span data-stu-id="d263c-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="d263c-113">Par défaut, la version de l’assembly spécifiée dans le manifeste est la version utilisée lors de l’activation.</span><span class="sxs-lookup"><span data-stu-id="d263c-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="d263c-114">La configuration globale de l’application spécifie la configuration de toutes les applications sur le système.</span><span class="sxs-lookup"><span data-stu-id="d263c-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="d263c-115">La configuration par application peut remplacer la configuration d’application globale pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="d263c-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="d263c-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifeste de configuration de l’application**</span><span class="sxs-lookup"><span data-stu-id="d263c-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="d263c-117">Fichier qui spécifie les assemblys côte à côte à utiliser par une application totalement ou partiellement isolée.</span><span class="sxs-lookup"><span data-stu-id="d263c-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="d263c-118">Les fichiers manifeste de la configuration de l’application sont installés dans le même dossier que le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="d263c-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="d263c-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifeste d’application**</span><span class="sxs-lookup"><span data-stu-id="d263c-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="d263c-120">Fichier qui décrit une application isolée.</span><span class="sxs-lookup"><span data-stu-id="d263c-120">File that describes an isolated application.</span></span> <span data-ttu-id="d263c-121">Il spécifie les informations requises pour exécuter l’application, y compris les dépendances sur les assemblys privés, les versions spécifiques des assemblys partagés et les métadonnées pour les assemblys privés.</span><span class="sxs-lookup"><span data-stu-id="d263c-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="d263c-122">Le nom d’un fichier manifeste d’application est le nom de l’exécutable de l’application suivi de l’extension. manifest.</span><span class="sxs-lookup"><span data-stu-id="d263c-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="d263c-123">Par exemple, pour MySampleApp.exe, le fichier manifeste est MySampleApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="d263c-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="d263c-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**chargeur**</span><span class="sxs-lookup"><span data-stu-id="d263c-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="d263c-125">Unité fondamentale pour l’affectation de noms, la liaison, le contrôle de version, le déploiement ou la configuration d’un bloc de code de programmation.</span><span class="sxs-lookup"><span data-stu-id="d263c-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="d263c-126">Ces assemblys de code peuvent être placés dans des dll ou des assemblys COM.</span><span class="sxs-lookup"><span data-stu-id="d263c-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="d263c-127">Les applications avec des fonctionnalités communes peuvent exécuter des blocs partagés de code de programmation, appelés modules ou assemblys de code.</span><span class="sxs-lookup"><span data-stu-id="d263c-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="d263c-128">L’infrastructure pour le partage sécurisé des assemblys est appelée partage d’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d263c-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="d263c-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifeste d’assembly**</span><span class="sxs-lookup"><span data-stu-id="d263c-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="d263c-130">Description d’un assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d263c-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="d263c-131">Il spécifie le nom, la version, les fichiers, les ressources de l’assembly, les données de liaison pour les éléments de l’assembly et les dépendances sur d’autres assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d263c-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="d263c-132">Un fichier manifeste d’assembly peut avoir n’importe quel nom de fichier valide, à condition qu’il soit suivi par l’extension. manifest.</span><span class="sxs-lookup"><span data-stu-id="d263c-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



