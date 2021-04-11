---
description: Gérer le partage d’assemblys et le contrôle de version des DLL dans le magasin d’assemblys côte à côte des systèmes à partir de programmes. Écrivez des manifestes d’assembly et des applications auto-descriptives pour le partage d’assembly et la redirection des dll.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Applications isolées et assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112706"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="134f1-104">Applications isolées et assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="134f1-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="134f1-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="134f1-105">Purpose</span></span>

<span data-ttu-id="134f1-106">Les applications isolées et les assemblys côte à côte sont une solution Microsoft Windows qui réduit les conflits de contrôle de version dans les applications clientes Windows.</span><span class="sxs-lookup"><span data-stu-id="134f1-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="134f1-107">Avec Windows, les développeurs d’applications peuvent créer des applications isolées qui sont entièrement explicites et non affectées par des modifications apportées au registre, à d’autres applications ou à d’autres versions d’assemblys s’exécutant sur le système.</span><span class="sxs-lookup"><span data-stu-id="134f1-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="134f1-108">Les créateurs d’applications et les administrateurs peuvent utiliser des manifestes pour gérer le partage d’assemblys côte à côte après le déploiement, au niveau global ou par application.</span><span class="sxs-lookup"><span data-stu-id="134f1-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="134f1-109">Les clients bénéficient d’applications isolées qui sont plus stables et mises à jour de manière plus fiable.</span><span class="sxs-lookup"><span data-stu-id="134f1-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="134f1-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="134f1-110">Where applicable</span></span>

<span data-ttu-id="134f1-111">Les applications isolées et le partage d’assembly côte à côte peuvent être utilisés pour développer des applications qui partagent en toute sécurité des assemblys de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="134f1-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="134f1-112">Les développeurs peuvent utiliser cette technologie pour corriger les conflits de contrôle de version des DLL causés par une version incompatible d’un assembly partagé.</span><span class="sxs-lookup"><span data-stu-id="134f1-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="134f1-113">Si votre application doit toujours obtenir la version d’un composant que vous avez testé, il est possible d’isoler votre application afin qu’elle s’exécute toujours avec la version testée du composant sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="134f1-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="134f1-114">Les applications isolées et les assemblys côte à côte sont destinés au développement d’applications de style bureau.</span><span class="sxs-lookup"><span data-stu-id="134f1-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="134f1-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="134f1-115">Developer audience</span></span>

<span data-ttu-id="134f1-116">Cette documentation est destinée principalement aux développeurs de logiciels, aux développeurs d’applications et aux administrateurs réseau :</span><span class="sxs-lookup"><span data-stu-id="134f1-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="134f1-117">Les développeurs de logiciels qui souhaitent créer des applications isolées qui utiliseront les assemblys côte à côte mis à disposition par Microsoft et d’autres éditeurs d’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="134f1-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="134f1-118">Les développeurs d’applications qui souhaitent créer leurs propres assemblys côte à côte pour isoler leurs applications.</span><span class="sxs-lookup"><span data-stu-id="134f1-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="134f1-119">Administrateurs réseau qui souhaitent obtenir des informations supplémentaires sur les applications isolées.</span><span class="sxs-lookup"><span data-stu-id="134f1-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="134f1-120">En tant que référence principale pour le partage d’assembly côte à côte et les applications isolées, cette documentation fournit des informations générales sur la création de manifestes et d’assemblys côte à côte, l’installation d’applications isolées et d’assemblys côte à côte, et l’utilisation de l’API de contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="134f1-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="134f1-121">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="134f1-121">Run-time requirements</span></span>

<span data-ttu-id="134f1-122">Windows Server 2003 et versions ultérieures, ou Windows XP et versions ultérieures, sont requis pour utiliser des manifestes et des assemblys côte à côte afin d’isoler les applications et d’utiliser l’API de contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="134f1-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="134f1-123">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="134f1-123">In this section</span></span>



| <span data-ttu-id="134f1-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="134f1-124">Topic</span></span>                                                         | <span data-ttu-id="134f1-125">Description</span><span class="sxs-lookup"><span data-stu-id="134f1-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="134f1-126">Référence</span><span class="sxs-lookup"><span data-stu-id="134f1-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="134f1-127">Documentation des applications isolées et des assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="134f1-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 




