---
description: L’API de regroupement pair combine la technologie de l’API du fournisseur d’espace de noms PNRP et l’API de graphique.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: À propos de l’API de regroupement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543501"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="96798-103">À propos de l’API de regroupement</span><span class="sxs-lookup"><span data-stu-id="96798-103">About the Grouping API</span></span>

<span data-ttu-id="96798-104">L’API de regroupement pair combine la technologie de l' [API du fournisseur d’espace de noms PNRP](pnrp-namespace-provider-api.md) et l' [API de graphique](graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="96798-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="96798-105">Le regroupement ajoute les deux technologies suivantes :</span><span class="sxs-lookup"><span data-stu-id="96798-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="96798-106">Couche de multiplexage qui permet à plusieurs applications d’utiliser un graphique, un port et une base de données d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="96798-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="96798-107">La sécurité qui garantit que seuls les homologues invités à un groupe peuvent rejoindre et se connecter pendant toute la durée de vie d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="96798-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="96798-108">Le regroupement offre une approche accessible et facile aux réseaux homologues en raison du flot d’appels simple et de la messagerie sécurisée.</span><span class="sxs-lookup"><span data-stu-id="96798-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="96798-109">Cette API utilise PNRP pour la découverte de groupes et un fournisseur de sécurité standard basé sur l’infrastructure à clé publique au lieu de demander à un développeur d’en implémenter un.</span><span class="sxs-lookup"><span data-stu-id="96798-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="96798-110">Toutefois, si votre application exige une plus grande flexibilité en termes d’options de sécurité, envisagez d’utiliser l' [API Graph](about-the-graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="96798-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="96798-111">Le tableau suivant répertorie les rubriques de cette section de l’API de regroupement :</span><span class="sxs-lookup"><span data-stu-id="96798-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="96798-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="96798-112">Topic</span></span>                                                                | <span data-ttu-id="96798-113">Description</span><span class="sxs-lookup"><span data-stu-id="96798-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96798-114">Utilisation des groupes</span><span class="sxs-lookup"><span data-stu-id="96798-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="96798-115">Décrit le workflow d’appel dans une application de regroupement d’homologues du démarrage à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="96798-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="96798-116">Fonctionnement de la sécurité de groupe</span><span class="sxs-lookup"><span data-stu-id="96798-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="96798-117">Décrit le mode de sécurisation de l’appartenance aux groupes homologues et des échanges de données.</span><span class="sxs-lookup"><span data-stu-id="96798-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="96798-118">Invitation d’un pair à un groupe</span><span class="sxs-lookup"><span data-stu-id="96798-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="96798-119">Décrit le processus par lequel les homologues sont invités et ajoutés à un groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="96798-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="96798-120">Comment se connecter à un groupe homologue</span><span class="sxs-lookup"><span data-stu-id="96798-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="96798-121">Décrit comment un homologue se connecte à un groupe homologue et interagit avec lui.</span><span class="sxs-lookup"><span data-stu-id="96798-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="96798-122">Gestion des enregistrements de groupe</span><span class="sxs-lookup"><span data-stu-id="96798-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="96798-123">Décrit les enregistrements de groupe homologue et comment les gérer en tant que membre et en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="96798-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="96798-124">Les applications qui utilisent l’API de regroupement dans un environnement avec un pare-feu nécessitent des groupes d’exceptions qui couvrent le port propre à l’application, ainsi que le port « 3587-TCP » pour l’API de regroupement et le port « 3540-UDP » pour PNRP.</span><span class="sxs-lookup"><span data-stu-id="96798-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="96798-125">Ces groupes d’exceptions doivent être activés chaque fois que l’application est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="96798-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



