---
title: Interfaces de service Active Directory
description: Présentation des interfaces des services de Active Directory, avec des liens vers différents guides.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfaces de service Active Directory (voir ADSI)
- ADSI ADSI, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031855"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="a5b39-106">Interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5b39-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="a5b39-107">Objectif</span><span class="sxs-lookup"><span data-stu-id="a5b39-107">Purpose</span></span>

<span data-ttu-id="a5b39-108">Les interfaces ADSI (Active Directory Service Interfaces) sont un ensemble d’interfaces COM utilisées pour accéder aux fonctionnalités des services d’annuaire à partir de différents fournisseurs de réseau.</span><span class="sxs-lookup"><span data-stu-id="a5b39-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="a5b39-109">ADSI est utilisé dans un environnement informatique distribué pour présenter un ensemble unique d’interfaces de service d’annuaire pour la gestion des ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="a5b39-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="a5b39-110">Les administrateurs et les développeurs peuvent utiliser les services ADSI pour énumérer et gérer les ressources dans un service d’annuaire, quel que soit l’environnement réseau qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="a5b39-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="a5b39-111">ADSI permet des tâches d’administration courantes, telles que l’ajout de nouveaux utilisateurs, la gestion des imprimantes et la localisation des ressources dans un environnement informatique distribué.</span><span class="sxs-lookup"><span data-stu-id="a5b39-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="a5b39-112">La documentation suivante est destinée aux programmeurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="a5b39-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="a5b39-113">Si vous êtes un utilisateur final qui tente de déboguer une erreur d’impression ou un problème de réseau à distance, consultez les forums de la [communauté Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a5b39-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="a5b39-114">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="a5b39-114">Where applicable</span></span>

<span data-ttu-id="a5b39-115">Les administrateurs réseau peuvent utiliser ADSI pour automatiser les tâches courantes, telles que l’ajout d’utilisateurs et de groupes, la gestion des imprimantes et la définition d’autorisations sur les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="a5b39-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="a5b39-116">Les éditeurs de logiciels indépendants et les développeurs d’utilisateurs finaux peuvent utiliser ADSI pour « activer l’annuaire » de leurs produits et applications.</span><span class="sxs-lookup"><span data-stu-id="a5b39-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="a5b39-117">Les services peuvent se publier eux-mêmes dans un répertoire, les clients peuvent utiliser l’annuaire pour rechercher les services, et les deux peuvent utiliser le répertoire pour rechercher et manipuler d’autres objets intéressants.</span><span class="sxs-lookup"><span data-stu-id="a5b39-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="a5b39-118">Étant donné que les interfaces de service Active Directory sont indépendantes des services d’annuaire sous-jacents, les produits et les applications compatibles avec l’annuaire peuvent fonctionner correctement dans plusieurs environnements réseau et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a5b39-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a5b39-119">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a5b39-119">Developer audience</span></span>

<span data-ttu-id="a5b39-120">Vous pouvez écrire des applications clientes ADSI dans de nombreux langages.</span><span class="sxs-lookup"><span data-stu-id="a5b39-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="a5b39-121">Pour la plupart des tâches d’administration, ADSI définit des interfaces et des objets accessibles à partir de langages compatibles Automation tels que Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) et Java à des langages de performances et d’efficacité plus sensibles, tels que C et C++.</span><span class="sxs-lookup"><span data-stu-id="a5b39-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="a5b39-122">Une bonne base de la programmation COM est utile pour le programmeur ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5b39-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a5b39-123">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="a5b39-123">Run-time requirements</span></span>

<span data-ttu-id="a5b39-124">Active Directory s’exécute sur les contrôleurs de domaine Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a5b39-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="a5b39-125">Toutefois, les applications clientes utilisant ADSI peuvent être écrites et exécutées sur Windows.</span><span class="sxs-lookup"><span data-stu-id="a5b39-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="a5b39-126">En outre, les développeurs souhaiteront le kit de développement logiciel (SDK) de la plateforme, également disponible sur le site Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="a5b39-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="a5b39-127">Pour examiner le contenu de Active Directory, utilisez le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a5b39-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="a5b39-128">Ce composant logiciel enfichable remplace l’outil ADSVW disponible pour les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="a5b39-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a5b39-129">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a5b39-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a5b39-130">À propos d’ADSI</span><span class="sxs-lookup"><span data-stu-id="a5b39-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="a5b39-131">Informations générales sur ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5b39-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="a5b39-132">Utilisation d’ADSI</span><span class="sxs-lookup"><span data-stu-id="a5b39-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="a5b39-133">Guide de programmation de l’utilisation d’ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5b39-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="a5b39-134">Didacticiels de démarrage rapide ADSI</span><span class="sxs-lookup"><span data-stu-id="a5b39-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="a5b39-135">Utilisation d’ADSI avec Automation pour gérer les répertoires.</span><span class="sxs-lookup"><span data-stu-id="a5b39-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="a5b39-136">Référence ADSI</span><span class="sxs-lookup"><span data-stu-id="a5b39-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="a5b39-137">Documentation des interfaces et des méthodes ADSI.</span><span class="sxs-lookup"><span data-stu-id="a5b39-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a5b39-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5b39-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b39-139">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="a5b39-139">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> <dt>

[<span data-ttu-id="a5b39-140">Clients et serveurs COM</span><span class="sxs-lookup"><span data-stu-id="a5b39-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="a5b39-141">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a5b39-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 