---
description: Les assemblys côte à côte sont utilisés avec les types de manifestes et de fichiers de configuration suivants. Les manifestes et les configurations sont des fichiers XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Référence des fichiers manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112703"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="b421b-104">Référence des fichiers manifeste</span><span class="sxs-lookup"><span data-stu-id="b421b-104">Manifest Files Reference</span></span>

<span data-ttu-id="b421b-105">Les assemblys côte à côte sont utilisés avec les types de manifestes et de fichiers de configuration suivants.</span><span class="sxs-lookup"><span data-stu-id="b421b-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="b421b-106">Les manifestes et les configurations sont des fichiers XML.</span><span class="sxs-lookup"><span data-stu-id="b421b-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="b421b-107">Manifeste</span><span class="sxs-lookup"><span data-stu-id="b421b-107">Manifest</span></span>                                                               | <span data-ttu-id="b421b-108">Description</span><span class="sxs-lookup"><span data-stu-id="b421b-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b421b-109">Manifestes d’assembly</span><span class="sxs-lookup"><span data-stu-id="b421b-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="b421b-110">Décrit les noms, les versions, les ressources et les dépendances d’assembly des assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="b421b-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="b421b-111">Manifestes d’application</span><span class="sxs-lookup"><span data-stu-id="b421b-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="b421b-112">Décrit les noms et les versions des assemblys partagés côte à côte auxquels l’application doit se lier au moment de l’exécution et peut également contenir des métadonnées pour les assemblys côte à côte privés utilisés par l’application.</span><span class="sxs-lookup"><span data-stu-id="b421b-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="b421b-113">Fichiers de configuration de l’application</span><span class="sxs-lookup"><span data-stu-id="b421b-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="b421b-114">Redirige les versions d’assembly des dépendances d’assembly à l’aide de la [configuration par application](per-application-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="b421b-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="b421b-115">Fichiers de configuration du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="b421b-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="b421b-116">Redirige les versions d’assembly des dépendances d’assembly sur la base de chaque assembly à l’aide d’une [configuration d’éditeur](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="b421b-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="b421b-117">Pour obtenir la liste du schéma de fichier manifeste, consultez [schéma de fichier manifeste](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b421b-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="b421b-118">Pour obtenir la liste du schéma de fichier de configuration de l’application, consultez [schéma du fichier de configuration](application-configuration-file-schema.md)de l’application.</span><span class="sxs-lookup"><span data-stu-id="b421b-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="b421b-119">Pour obtenir la liste du schéma du fichier de configuration du serveur de publication, consultez [schéma du fichier de configuration](publisher-configuration-file-schema.md)de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="b421b-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="b421b-120">D’autres technologies étendent le format utilisé par les manifestes de version et de configuration de Windows.</span><span class="sxs-lookup"><span data-stu-id="b421b-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="b421b-121">Les développeurs doivent se référer à la documentation spécifique à la technologie utilisée pour obtenir des informations sur le format du manifeste.</span><span class="sxs-lookup"><span data-stu-id="b421b-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="b421b-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b421b-122">For example:</span></span>

-   [<span data-ttu-id="b421b-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="b421b-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="b421b-124">Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="b421b-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="b421b-125">[Contrôle de compte d'utilisateur (UAC)](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b421b-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 
