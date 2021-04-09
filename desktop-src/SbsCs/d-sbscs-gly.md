---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: D (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8912f24478f79be8aa00c963dc27cb46ec756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034638"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="12854-103">D (applications isolées et assemblys côte à côte)</span><span class="sxs-lookup"><span data-stu-id="12854-103">D (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="12854-104">[A](a-sbscs-gly.md) B C D e F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="12854-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="12854-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**Texte de définition de contexte DEF**</span><span class="sxs-lookup"><span data-stu-id="12854-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-context assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="12854-106">Sous-élément **assemblyIdentity** définissant l’assembly côte à côte décrit par le manifeste.</span><span class="sxs-lookup"><span data-stu-id="12854-106">An **assemblyIdentity** subelement defining the side-by-side assembly described by the manifest.</span></span> <span data-ttu-id="12854-107">Un sous-élément **assemblyIdentity** de contexte de définition est toujours le premier sous-élément d’un élément d' **assembly** .</span><span class="sxs-lookup"><span data-stu-id="12854-107">A DEF-context **assemblyIdentity** subelement is always the first subelement of an **assembly** element.</span></span>

</dd> <dt>

<span data-ttu-id="12854-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**Conflit de versions de DLL**</span><span class="sxs-lookup"><span data-stu-id="12854-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL versioning conflict**</span></span>
</dt> <dd>

<span data-ttu-id="12854-109">Problème de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="12854-109">Compatibility problem.</span></span> <span data-ttu-id="12854-110">Des problèmes de partage d’assemblys se produisent quand une application installe une version d’un assembly partagé qui n’est pas à compatibilité descendante avec la version installée précédemment.</span><span class="sxs-lookup"><span data-stu-id="12854-110">Assembly sharing problems occur when an application installs a version of a shared assembly that is not backward compatible with the previously installed version.</span></span> <span data-ttu-id="12854-111">Une solution aux conflits de contrôle de version des DLL consiste à utiliser le partage d’assembly côte à côte et des applications isolées.</span><span class="sxs-lookup"><span data-stu-id="12854-111">A solution to DLL versioning conflicts is to use side-by-side assembly sharing and isolated applications.</span></span> <span data-ttu-id="12854-112">Avec le partage d’assembly côte à côte, plusieurs versions du même assembly Windows peuvent s’exécuter simultanément.</span><span class="sxs-lookup"><span data-stu-id="12854-112">With side-by-side assembly sharing, multiple versions of the same Windows assembly can run simultaneously.</span></span> <span data-ttu-id="12854-113">Les développeurs peuvent choisir l’assembly côte à côte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="12854-113">Developers can choose which side-by-side assembly to use.</span></span>

</dd> </dl>

 

 



