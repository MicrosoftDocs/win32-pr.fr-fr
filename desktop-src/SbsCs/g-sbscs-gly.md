---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: G (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516854"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="a24bd-103">G (applications isolées et assemblys côte à côte)</span><span class="sxs-lookup"><span data-stu-id="a24bd-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="a24bd-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) e F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="a24bd-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a24bd-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**Configuration globale de l’application**</span><span class="sxs-lookup"><span data-stu-id="a24bd-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="a24bd-106">Spécification que toutes les applications sur le système utilisent la même version d’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="a24bd-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="a24bd-107">La configuration globale est spécifiée par assembly dans un fichier manifeste d’assembly global installé dans le dossier WinSxS.</span><span class="sxs-lookup"><span data-stu-id="a24bd-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="a24bd-108">La configuration globale peut être utilisée lorsqu’un développeur ou un administrateur d’assembly doit configurer toutes les applications sur le système pour utiliser une version d’assembly plus récente.</span><span class="sxs-lookup"><span data-stu-id="a24bd-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="a24bd-109">Dans ce cas, le nouvel assembly doit être à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="a24bd-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="a24bd-110">Une configuration par application remplace la configuration d’application par défaut ou globale pour des applications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a24bd-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="a24bd-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**manifeste d’assembly global**</span><span class="sxs-lookup"><span data-stu-id="a24bd-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="a24bd-112">Fichier qui définit la configuration d’application globale d’un assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="a24bd-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="a24bd-113">Les fichiers manifestes de l’assembly global sont installés dans le magasin de l’assembly système dans le dossier WinSxS.</span><span class="sxs-lookup"><span data-stu-id="a24bd-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



