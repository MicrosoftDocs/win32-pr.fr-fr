---
description: Le catalogue COM+ stocke les attributs d’application COM+, les attributs de classe et les attributs au niveau de l’ordinateur. Il garantit la cohérence entre ces attributs et fournit des opérations courantes en plus de ces attributs.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516367"
---
# <a name="the-com-catalog"></a><span data-ttu-id="aaf94-104">Le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="aaf94-104">The COM+ Catalog</span></span>

<span data-ttu-id="aaf94-105">Le catalogue COM+ stocke les attributs d’application COM+, les attributs de classe et les attributs au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="aaf94-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="aaf94-106">Il garantit la cohérence entre ces attributs et fournit des opérations courantes en plus de ces attributs.</span><span class="sxs-lookup"><span data-stu-id="aaf94-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="aaf94-107">Le catalogue COM+ utilise deux magasins différents, comme suit :</span><span class="sxs-lookup"><span data-stu-id="aaf94-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="aaf94-108">La base de données d’inscription COM+</span><span class="sxs-lookup"><span data-stu-id="aaf94-108">The COM+ registration database</span></span>
-   <span data-ttu-id="aaf94-109">Le Registre Windows (**HKEY \_ classes \_ root**)</span><span class="sxs-lookup"><span data-stu-id="aaf94-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="aaf94-110">Le catalogue présente une vue logique et unifiée de ces deux magasins et les expose via la bibliothèque d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="aaf94-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="aaf94-111">Cette bibliothèque fournit, via un langage de script, toutes les fonctionnalités de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="aaf94-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="aaf94-112">Pour les composants COM existants qui ne nécessitent pas de nouveaux services COM+, la recherche s’effectue dans le Registre Windows existant.</span><span class="sxs-lookup"><span data-stu-id="aaf94-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="aaf94-113">Le catalogue COM+ utilise également le Registre Windows pour la bibliothèque de types et l’inscription de proxy/stub d’interface.</span><span class="sxs-lookup"><span data-stu-id="aaf94-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="aaf94-114">Fractionner l’inscription</span><span class="sxs-lookup"><span data-stu-id="aaf94-114">Split Registration</span></span>

<span data-ttu-id="aaf94-115">Pour les nouveaux composants qui sont déjà des composants COM existants qui sont utilisés dans l’environnement de services (par exemple, les composants MTS), l’aspect COM de base de l’inscription est stocké dans le Registre Windows et les nouveaux services et attributs (par exemple, les composants mis en file d’attente) sont stockés dans la base de données d’inscription COM+.</span><span class="sxs-lookup"><span data-stu-id="aaf94-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="aaf94-116">C’est ce qu’on appelle une *inscription fractionnée*.</span><span class="sxs-lookup"><span data-stu-id="aaf94-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="aaf94-117">Chaque attribut est stocké dans un seul emplacement : le Registre Windows ou la base de données d’inscription COM+.</span><span class="sxs-lookup"><span data-stu-id="aaf94-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="aaf94-118">Les nouveaux composants COM sont inscrits exclusivement dans la base de données d’inscription COM+, avec une certaine duplication dans le Registre Windows afin que les outils existants puissent les utiliser.</span><span class="sxs-lookup"><span data-stu-id="aaf94-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="aaf94-119">Mises à jour transactionnelles du catalogue</span><span class="sxs-lookup"><span data-stu-id="aaf94-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="aaf94-120">Certaines opérations sur le catalogue sont effectuées de manière transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="aaf94-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="aaf94-121">Lorsque vous appelez la bibliothèque d’administration COM+ à partir d’un composant transactionnel, les mises à jour apportées à la base de données d’inscription COM+ se produisent dans la limite de transaction du composant appelant.</span><span class="sxs-lookup"><span data-stu-id="aaf94-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="aaf94-122">Toutefois, il n’est pas garanti que les mises à jour qui impliquent des modifications d’autres magasins (telles que le système de fichiers et le Registre Windows) soient entièrement transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="aaf94-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="aaf94-123">Une transaction abandonnée peut conserver ces magasins dans un état incohérent avec les modifications apportées à l’un ou à la base de données d’inscription COM+.</span><span class="sxs-lookup"><span data-stu-id="aaf94-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaf94-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aaf94-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf94-125">Création de packages d’installation pour les applications COM+</span><span class="sxs-lookup"><span data-stu-id="aaf94-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="aaf94-126">Déploiement de proxys d’application</span><span class="sxs-lookup"><span data-stu-id="aaf94-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="aaf94-127">L’utilitaire de réplication COMREPL</span><span class="sxs-lookup"><span data-stu-id="aaf94-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



