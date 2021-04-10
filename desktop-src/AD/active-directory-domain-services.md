---
title: Services de domaine Active Directory
description: Microsoft Active Directory Domain Services sont la base des réseaux distribués basés sur les systèmes d’exploitation Windows 2000 Server, Windows Server 2003 et Microsoft Windows Server 2008 qui utilisent des contrôleurs de domaine.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, page de démarrage
- Active Directory Domain Services Active Directory, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032060"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="f2f98-106">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="f2f98-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="f2f98-107">Objectif</span><span class="sxs-lookup"><span data-stu-id="f2f98-107">Purpose</span></span>

<span data-ttu-id="f2f98-108">Microsoft Active Directory Domain Services sont la base des réseaux distribués basés sur les systèmes d’exploitation Windows 2000 Server, Windows Server 2003 et Microsoft Windows Server 2008 qui utilisent des contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="f2f98-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="f2f98-109">Active Directory Domain Services fournir un stockage de données hiérarchique, sécurisé et structuré pour les objets d’un réseau, tels que les utilisateurs, les ordinateurs, les imprimantes et les services.</span><span class="sxs-lookup"><span data-stu-id="f2f98-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="f2f98-110">Active Directory Domain Services prennent en charge la localisation et l’utilisation de ces objets.</span><span class="sxs-lookup"><span data-stu-id="f2f98-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="f2f98-111">Ce guide fournit une vue d’ensemble des Active Directory Domain Services et des exemples de code pour les tâches de base, telles que la recherche d’objets et la lecture des propriétés, pour des tâches plus avancées telles que la publication de service.</span><span class="sxs-lookup"><span data-stu-id="f2f98-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="f2f98-112">Windows 2000 Server et les systèmes d’exploitation ultérieurs fournissent une interface utilisateur permettant aux utilisateurs et aux administrateurs de travailler avec les objets et les données de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f2f98-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="f2f98-113">Ce guide décrit comment étendre et personnaliser cette interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f2f98-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="f2f98-114">Elle explique également comment étendre les Active Directory Domain Services en définissant de nouvelles classes et attributs d’objet.</span><span class="sxs-lookup"><span data-stu-id="f2f98-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="f2f98-115">La documentation suivante est destinée aux programmeurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="f2f98-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="f2f98-116">Si vous êtes un utilisateur final qui tente de déboguer une erreur d’impression ou un problème de réseau à distance, consultez les forums de la [communauté Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f2f98-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="f2f98-117">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="f2f98-117">Where applicable</span></span>

<span data-ttu-id="f2f98-118">Les administrateurs réseau écrivent des scripts et des applications qui accèdent à Active Directory Domain Services pour automatiser les tâches administratives courantes, telles que l’ajout d’utilisateurs et de groupes, la gestion des imprimantes et la définition d’autorisations pour les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="f2f98-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="f2f98-119">Les éditeurs de logiciels indépendants et les développeurs d’utilisateurs finaux peuvent utiliser Active Directory Domain Services programmation pour activer l’annuaire de leurs produits et applications.</span><span class="sxs-lookup"><span data-stu-id="f2f98-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="f2f98-120">Les services peuvent se publier eux-mêmes dans Active Directory Domain Services ; les clients peuvent utiliser Active Directory Domain Services pour rechercher des services, et les deux peuvent utiliser Active Directory Domain Services pour rechercher et utiliser d’autres objets sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="f2f98-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f2f98-121">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="f2f98-121">Developer audience</span></span>

<span data-ttu-id="f2f98-122">Les applications qui accèdent aux données dans Active Directory Domain Services peuvent être écrites à l’aide de l’API [interfaces de Service Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , de l’API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) ou de l’espace de noms [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="f2f98-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f2f98-123">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="f2f98-123">Run-time requirements</span></span>

<span data-ttu-id="f2f98-124">Active Directory Domain Services s’exécuter sur les contrôleurs de domaine Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f2f98-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="f2f98-125">Toutefois, les applications clientes peuvent être écrites pour et s’exécuter sous Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 et Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f2f98-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2f98-126">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f2f98-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f2f98-127">À propos de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="f2f98-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="f2f98-128">Informations générales sur Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f2f98-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="f2f98-129">Utilisation des services de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="f2f98-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="f2f98-130">Guide de programmation Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f2f98-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="f2f98-131">Référence Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="f2f98-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="f2f98-132">Référence de programmation de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f2f98-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 