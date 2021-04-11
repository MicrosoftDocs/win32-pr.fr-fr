---
title: Exemples d’applications (infrastructure d’homologue)
description: Les exemples d’applications suivants sont inclus dans le kit de développement logiciel (SDK) homologue Windows XP.
ms.assetid: 26c45360-f232-4e29-90b5-44ccacb5a9c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15e2bf3162151a4cbf18547fdfe482c7ea77fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952028"
---
# <a name="sample-applications-peer-infrastructure"></a><span data-ttu-id="e4489-103">Exemples d’applications (infrastructure d’homologue)</span><span class="sxs-lookup"><span data-stu-id="e4489-103">Sample applications (Peer Infrastructure)</span></span>

<span data-ttu-id="e4489-104">Les exemples d’applications suivants sont inclus dans le kit de développement logiciel (SDK) homologue Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4489-104">The following sample applications are included in the Windows XP Peer SDK.</span></span> <span data-ttu-id="e4489-105">Les exemples peuvent vous aider quand vous développez vos propres applications homologues à l’aide de l’infrastructure homologue.</span><span class="sxs-lookup"><span data-stu-id="e4489-105">The samples can help you when you develop your own peer applications using the Peer Infrastructure.</span></span>

-   [<span data-ttu-id="e4489-106">Conversation Graph</span><span class="sxs-lookup"><span data-stu-id="e4489-106">Graph Chat</span></span>](#graph-chat)
-   [<span data-ttu-id="e4489-107">Conversation de groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-107">Group Chat</span></span>](#group-chat)
-   [<span data-ttu-id="e4489-108">Explorateur de groupes</span><span class="sxs-lookup"><span data-stu-id="e4489-108">Group Browser</span></span>](#group-browser)

## <a name="graph-chat"></a><span data-ttu-id="e4489-109">Conversation Graph</span><span class="sxs-lookup"><span data-stu-id="e4489-109">Graph Chat</span></span>

<span data-ttu-id="e4489-110">L’exemple d’application Graph chat est une simple application de conversation qui montre comment utiliser les API Graph Peer et le fournisseur d’espace de noms PNRP (Peer Name Resolution Protocol) avec l’API Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="e4489-110">The Graph Chat sample application is a simple chat application that demonstrates how to use the Peer Graphing APIs and the Peer Name Resolution Protocol (PNRP) Namespace Provider with the Winsock 2 API.</span></span> <span data-ttu-id="e4489-111">L’application illustre les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4489-111">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="e4489-112">Création d’un graphique</span><span class="sxs-lookup"><span data-stu-id="e4489-112">Creating a graph</span></span>
-   <span data-ttu-id="e4489-113">Connexion à un graphique existant</span><span class="sxs-lookup"><span data-stu-id="e4489-113">Connecting to an existing graph</span></span>
-   <span data-ttu-id="e4489-114">Déconnexion d’un graphique existant</span><span class="sxs-lookup"><span data-stu-id="e4489-114">Disconnecting from an existing graph</span></span>
-   <span data-ttu-id="e4489-115">Énumération des entités homologues</span><span class="sxs-lookup"><span data-stu-id="e4489-115">Enumerating peer entities</span></span>
-   <span data-ttu-id="e4489-116">Ajout d’enregistrements au graphique</span><span class="sxs-lookup"><span data-stu-id="e4489-116">Adding records to the graph</span></span>
-   <span data-ttu-id="e4489-117">Utilisation de connexions directes avec un graphique</span><span class="sxs-lookup"><span data-stu-id="e4489-117">Using direct connections with a graph</span></span>
-   <span data-ttu-id="e4489-118">Utilisation de l’infrastructure de notifications et d’événements avec des graphiques</span><span class="sxs-lookup"><span data-stu-id="e4489-118">Using the notification and event infrastructure with graphs</span></span>
-   <span data-ttu-id="e4489-119">Inscription de noms avec PNRP</span><span class="sxs-lookup"><span data-stu-id="e4489-119">Registering names with PNRP</span></span>
-   <span data-ttu-id="e4489-120">Résolution de noms avec PNRP</span><span class="sxs-lookup"><span data-stu-id="e4489-120">Resolving names with PNRP</span></span>
-   <span data-ttu-id="e4489-121">Annulation de l’inscription des noms avec PNRP</span><span class="sxs-lookup"><span data-stu-id="e4489-121">Unregistering names with PNRP</span></span>

## <a name="group-chat"></a><span data-ttu-id="e4489-122">Conversation de groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-122">Group Chat</span></span>

<span data-ttu-id="e4489-123">L’exemple d’application de conversation de groupe est une simple application de conversation qui montre comment utiliser les API de regroupement pair et Identity Manager.</span><span class="sxs-lookup"><span data-stu-id="e4489-123">The Group Chat sample application is a simple chat application that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="e4489-124">L’application illustre les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4489-124">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="e4489-125">Création d’une identité</span><span class="sxs-lookup"><span data-stu-id="e4489-125">Creating an identity</span></span>
-   <span data-ttu-id="e4489-126">Création et obtention des informations d’identité</span><span class="sxs-lookup"><span data-stu-id="e4489-126">Creating and obtaining identity information</span></span>
-   <span data-ttu-id="e4489-127">Énumération des identités</span><span class="sxs-lookup"><span data-stu-id="e4489-127">Enumerating identities</span></span>
-   <span data-ttu-id="e4489-128">Énumération des groupes associés à une identité</span><span class="sxs-lookup"><span data-stu-id="e4489-128">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="e4489-129">Création d’un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-129">Creating a group</span></span>
-   <span data-ttu-id="e4489-130">Création d’invitations pour un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-130">Creating invitations for a group</span></span>
-   <span data-ttu-id="e4489-131">Connexion à un groupe existant</span><span class="sxs-lookup"><span data-stu-id="e4489-131">Connecting to an existing group</span></span>
-   <span data-ttu-id="e4489-132">Déconnexion d’un groupe existant</span><span class="sxs-lookup"><span data-stu-id="e4489-132">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="e4489-133">Extraction d’informations à partir des propriétés de groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-133">Extracting information from the group properties</span></span>
-   <span data-ttu-id="e4489-134">Utilisation de connexions directes avec un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-134">Using direct connections with a group</span></span>
-   <span data-ttu-id="e4489-135">Utilisation des fonctions d’énumération dans un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-135">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="e4489-136">Énumération des membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-136">Enumerating group members</span></span>
-   <span data-ttu-id="e4489-137">Ajout d’enregistrements à un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-137">Adding records to a group</span></span>
-   <span data-ttu-id="e4489-138">Utilisation de l’infrastructure de notifications et d’événements avec des groupes</span><span class="sxs-lookup"><span data-stu-id="e4489-138">Using the notification and event infrastructure with groups</span></span>

## <a name="group-browser"></a><span data-ttu-id="e4489-139">Explorateur de groupes</span><span class="sxs-lookup"><span data-stu-id="e4489-139">Group Browser</span></span>

<span data-ttu-id="e4489-140">L’exemple d’application de l’Explorateur de groupes est un outil de gestion de groupe homologue simple qui montre comment utiliser les API de regroupement pair et Identity Manager.</span><span class="sxs-lookup"><span data-stu-id="e4489-140">The Group Browser sample application is a simple peer group management tool that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="e4489-141">L’application illustre les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4489-141">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="e4489-142">Énumération des clouds PNRP</span><span class="sxs-lookup"><span data-stu-id="e4489-142">Enumerating PNRP clouds</span></span>
-   <span data-ttu-id="e4489-143">Énumération des identités</span><span class="sxs-lookup"><span data-stu-id="e4489-143">Enumerating identities</span></span>
-   <span data-ttu-id="e4489-144">Énumération des groupes associés à une identité</span><span class="sxs-lookup"><span data-stu-id="e4489-144">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="e4489-145">Création et suppression d’identités</span><span class="sxs-lookup"><span data-stu-id="e4489-145">Creating and deleting identities</span></span>
-   <span data-ttu-id="e4489-146">Création d’un groupe et Association de ce groupe à une identité</span><span class="sxs-lookup"><span data-stu-id="e4489-146">Creating a group and associating it with an identity</span></span>
-   <span data-ttu-id="e4489-147">Création d’une invitation et enregistrement</span><span class="sxs-lookup"><span data-stu-id="e4489-147">Creating an invitation and saving it</span></span>
-   <span data-ttu-id="e4489-148">Ouverture d’une invitation et utilisation de celle-ci pour rejoindre un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-148">Opening an invitation and using it to join a group</span></span>
-   <span data-ttu-id="e4489-149">Suppression d’une identité et appartenance à un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-149">Deleting an identity and group membership</span></span>
-   <span data-ttu-id="e4489-150">Connexion à un groupe existant</span><span class="sxs-lookup"><span data-stu-id="e4489-150">Connecting to an existing group</span></span>
-   <span data-ttu-id="e4489-151">Déconnexion d’un groupe existant</span><span class="sxs-lookup"><span data-stu-id="e4489-151">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="e4489-152">Extraction d’informations à partir des propriétés de groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-152">Extracting information from group properties</span></span>
-   <span data-ttu-id="e4489-153">Utilisation des fonctions d’énumération dans un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-153">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="e4489-154">Énumération des membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="e4489-154">Enumerating group members</span></span>
-   <span data-ttu-id="e4489-155">Utilisation de l’infrastructure de notifications et d’événements avec des groupes</span><span class="sxs-lookup"><span data-stu-id="e4489-155">Using the notification and event infrastructure with groups</span></span>

 

 



