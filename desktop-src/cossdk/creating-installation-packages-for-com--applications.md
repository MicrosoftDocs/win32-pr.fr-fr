---
description: Création de packages d’installation pour les applications COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Création de packages d’installation pour les applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516177"
---
# <a name="creating-installation-packages-for-com-applications"></a><span data-ttu-id="bc3e9-103">Création de packages d’installation pour les applications COM+</span><span class="sxs-lookup"><span data-stu-id="bc3e9-103">Creating Installation Packages for COM+ Applications</span></span>

<span data-ttu-id="bc3e9-104">Vous pouvez utiliser l’outil d’administration Services de composants ou la bibliothèque d’administration COM+ pour créer des packages d’installation pour les applications COM+ et les proxys d’application.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-104">You can use the Component Services administrative tool or the COM+ Administration Library to create installation packages for COM+ applications and application proxies.</span></span>

<span data-ttu-id="bc3e9-105">COM+ génère des packages d’installation Windows Installer, qui, dans un seul fichier, contiennent tous les éléments nécessaires pour installer une application COM+ sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-105">COM+ generates Windows Installer installation packages, which in a single file contain all the necessary pieces to install a COM+ application on another computer.</span></span>

<span data-ttu-id="bc3e9-106">Lors de l’exportation d’une application COM+, l’outil d’administration Services de composants détermine l’ensemble des classes, des composants et des attributs de l’application, ainsi que des attributs de niveau application.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-106">When exporting a COM+ application, the Component Services administrative tool determines the application's set of classes, components, and their attributes, as well as application-level attributes.</span></span> <span data-ttu-id="bc3e9-107">À partir de ces informations, l’outil d’administration Services de composants génère un seul fichier. msi, qui contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bc3e9-107">From this information, the Component Services administrative tool generates a single .msi file, which contains the following:</span></span>

-   <span data-ttu-id="bc3e9-108">Windows Installer des tables avec des informations d’inscription COM (pour plus d’informations, consultez la documentation de Windows Installer).</span><span class="sxs-lookup"><span data-stu-id="bc3e9-108">Windows Installer tables with COM registration information (see the Windows Installer documentation for details).</span></span>
-   <span data-ttu-id="bc3e9-109">Fichier. apl contenant les attributs de l’application.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-109">An .apl file containing the application's attributes.</span></span> <span data-ttu-id="bc3e9-110">(Il s’agit d’un fichier interne ; le format de ce fichier n’est pas documenté.)</span><span class="sxs-lookup"><span data-stu-id="bc3e9-110">(This is an internal file; the format of this file is not documented.)</span></span>
-   <span data-ttu-id="bc3e9-111">Bibliothèques de types et dll qui décrivent les interfaces implémentées par les classes de l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-111">DLLs and type libraries that describe the interfaces implemented by the COM+ application's classes.</span></span>

<span data-ttu-id="bc3e9-112">En plus du fichier. msi, l’outil d’administration Services de composants génère un fichier cabinet (. cab).</span><span class="sxs-lookup"><span data-stu-id="bc3e9-112">In addition to the .msi file, the Component Services administrative tool generates a cabinet (.cab) file.</span></span> <span data-ttu-id="bc3e9-113">Ce fichier encapsule le fichier. msi, ce qui permet au développeur de déployer l’application COM+ à l’aide de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-113">This file wraps the .msi file, allowing the developer to deploy the COM+ application through Microsoft Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="bc3e9-114">Lors de l’exportation d’une application COM+, l’outil d’administration Services de composants conditionne uniquement les parties COM+ standard de l’application.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-114">When exporting a COM+ application, the Component Services administrative tool packages only the standard COM+ parts of the application.</span></span> <span data-ttu-id="bc3e9-115">Il n’effectue pas de package, par exemple, les fichiers de données ou DLL dépendants.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-115">It does not package, for example, any dependent DLL or data files.</span></span> <span data-ttu-id="bc3e9-116">Les fichiers DLL dépendants doivent d’abord être installés sur un ordinateur avant l’installation de l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-116">The dependent DLL files must first be installed on a computer prior to installing the COM+ application.</span></span> <span data-ttu-id="bc3e9-117">Vous pouvez également utiliser l’outil de création de Windows Installer pour ajouter ces fichiers dépendants au fichier. msi généré par l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-117">Alternatively, you can use the Windows Installer authoring tool to add these dependent files to the .msi file generated by the Component Services administrative tool.</span></span> <span data-ttu-id="bc3e9-118">(Pour plus d’informations, consultez la documentation Windows Installer.)</span><span class="sxs-lookup"><span data-stu-id="bc3e9-118">(See the Windows Installer documentation for details.)</span></span>

 

## <a name="installing-com-applications-on-other-computers"></a><span data-ttu-id="bc3e9-119">Installation d’applications COM+ sur d’autres ordinateurs</span><span class="sxs-lookup"><span data-stu-id="bc3e9-119">Installing COM+ Applications on Other Computers</span></span>

<span data-ttu-id="bc3e9-120">Le fichier Windows Installer (. msi) généré par l’outil d’administration Services de composants peut être utilisé pour installer l’application COM+ sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-120">The Windows Installer (.msi) file generated by the Component Services administrative tool can be used to install the COM+ application on another computer.</span></span> <span data-ttu-id="bc3e9-121">Le fichier. msi contenant une application COM+ ne peut être installé que sur les ordinateurs qui prennent en charge les services COM+.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-121">The .msi file containing a COM+ application can be installed only on computers that support COM+ services.</span></span> <span data-ttu-id="bc3e9-122">Pour obtenir des procédures détaillées sur le déploiement d’applications COM+, voir la rubrique relative à l’installation des applications COM+ dans l’aide de l’administration des services de composants.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-122">For detailed procedures on deploying COM+ applications, see "Installing COM+ Applications," in the Component Services Administration Help.</span></span>

<span data-ttu-id="bc3e9-123">À moins que le fichier. msi ne soit modifié à l’aide d’un outil de création de Windows Installer, les applications COM+ installées à l’aide de la Windows Installer s’affichent dans le panneau de configuration Ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="bc3e9-123">Unless the .msi file is modified using a Windows Installer authoring tool, COM+ applications installed by using the Windows Installer appear in the Add/Remove Programs control panel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc3e9-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc3e9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc3e9-125">Déploiement de proxys d’application</span><span class="sxs-lookup"><span data-stu-id="bc3e9-125">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="bc3e9-126">Le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="bc3e9-126">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



