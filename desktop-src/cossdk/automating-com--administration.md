---
description: COM+ fournit un modèle objet d’administration qui expose toutes les fonctionnalités de l’outil d’administration Services de composants, lui-même un serveur frontal graphique écrit par-dessus les objets d’administration.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatisation de l’administration COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111047"
---
# <a name="automating-com-administration"></a><span data-ttu-id="0131c-103">Automatisation de l’administration COM+</span><span class="sxs-lookup"><span data-stu-id="0131c-103">Automating COM+ Administration</span></span>

<span data-ttu-id="0131c-104">COM+ fournit un modèle objet d’administration qui expose toutes les fonctionnalités de l’outil d’administration Services de composants, lui-même un serveur frontal graphique écrit par-dessus les objets d’administration.</span><span class="sxs-lookup"><span data-stu-id="0131c-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="0131c-105">Vous pouvez utiliser ces objets, fournis par la bibliothèque administration des services de composants (comadmin), pour automatiser toutes les tâches de l’administration des services et applications COM+.</span><span class="sxs-lookup"><span data-stu-id="0131c-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="0131c-106">Les objets comadmin vous permettent de lire et d’écrire des informations qui sont stockées sur le catalogue COM+, le magasin de données sous-jacent qui contient toutes les données de configuration COM+.</span><span class="sxs-lookup"><span data-stu-id="0131c-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="0131c-107">Vous pouvez utiliser ces objets pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0131c-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="0131c-108">Créez et configurez des applications COM+.</span><span class="sxs-lookup"><span data-stu-id="0131c-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="0131c-109">Installez et exportez les applications COM+ existantes.</span><span class="sxs-lookup"><span data-stu-id="0131c-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="0131c-110">Gérer les applications COM+ installées.</span><span class="sxs-lookup"><span data-stu-id="0131c-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="0131c-111">Gérez et configurez les services.</span><span class="sxs-lookup"><span data-stu-id="0131c-111">Manage and configure services.</span></span>
-   <span data-ttu-id="0131c-112">Administrer à distance les services de composants sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0131c-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="0131c-113">Vous pouvez utiliser les objets comadmins de scriptable avec n’importe quel langage compatible Automation, tel que Microsoft Visual Basic et Visual Basic Script.</span><span class="sxs-lookup"><span data-stu-id="0131c-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="0131c-114">Vous pouvez développer des scripts légers ou des outils d’administration à usage général.</span><span class="sxs-lookup"><span data-stu-id="0131c-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="0131c-115">Vous pouvez par exemple effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0131c-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="0131c-116">Écrire des scripts pour effectuer des tâches d’administration courantes.</span><span class="sxs-lookup"><span data-stu-id="0131c-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="0131c-117">Écrivez des scripts pour automatiser les processus dans le développement d’applications COM+.</span><span class="sxs-lookup"><span data-stu-id="0131c-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="0131c-118">Développez des outils à usage général pour l’administration et la surveillance des services de composants.</span><span class="sxs-lookup"><span data-stu-id="0131c-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="0131c-119">Développez des exécutables d’installation pour installer et déployer votre application COM+.</span><span class="sxs-lookup"><span data-stu-id="0131c-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="0131c-120">La bibliothèque comadmin offre une compatibilité descendante avec la bibliothèque d’administration MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="0131c-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="0131c-121">La plupart des codes d’administration MTS 2,0 existants continuent de fonctionner, bien qu’avec quelques exceptions.</span><span class="sxs-lookup"><span data-stu-id="0131c-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="0131c-122">(Voir [bibliothèque d’administration MTS](mts-administration-library.md).)</span><span class="sxs-lookup"><span data-stu-id="0131c-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="0131c-123">Pour automatiser efficacement l’administration, vous devez être familiarisé avec les tâches d’administration telles qu’elles sont effectuées avec l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="0131c-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="0131c-124">Pour obtenir une description complète des objets comadmin et des interfaces correspondantes, consultez la documentation de référence COM+ pour les classes et les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="0131c-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="0131c-125">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="0131c-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="0131c-126">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="0131c-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="0131c-127">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="0131c-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="0131c-128">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="0131c-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="0131c-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="0131c-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="0131c-130">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="0131c-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="0131c-131">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="0131c-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="0131c-132">Les rubriques suivantes de cette section fournissent une vue d’ensemble de l’automatisation de l’administration à l’aide des objets comadmin :</span><span class="sxs-lookup"><span data-stu-id="0131c-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="0131c-133">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="0131c-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="0131c-134">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="0131c-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="0131c-135">Définition des propriétés et enregistrement des modifications dans le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="0131c-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="0131c-136">Gestion des erreurs d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="0131c-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="0131c-137">Opérations d’administration COM+ dans les transactions</span><span class="sxs-lookup"><span data-stu-id="0131c-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="0131c-138">Exemple d’introduction utilisant le catalogue d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="0131c-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 



