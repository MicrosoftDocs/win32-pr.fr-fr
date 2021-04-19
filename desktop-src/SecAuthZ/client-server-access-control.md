---
description: Une application serveur fournit des services aux clients.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Access Control client/serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534382"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="f69b9-103">Access Control client/serveur</span><span class="sxs-lookup"><span data-stu-id="f69b9-103">Client/Server Access Control</span></span>

<span data-ttu-id="f69b9-104">Une application serveur fournit des services aux clients.</span><span class="sxs-lookup"><span data-stu-id="f69b9-104">A server application provides services to clients.</span></span> <span data-ttu-id="f69b9-105">Par exemple, un serveur peut effectuer les services suivants pour le compte d’un client :</span><span class="sxs-lookup"><span data-stu-id="f69b9-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="f69b9-106">Enregistrer et récupérer des informations à partir d’une base de données privée</span><span class="sxs-lookup"><span data-stu-id="f69b9-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="f69b9-107">Accéder aux ressources réseau</span><span class="sxs-lookup"><span data-stu-id="f69b9-107">Access network resources</span></span>
-   <span data-ttu-id="f69b9-108">Démarrer les [*processus*](/windows/desktop/SecGloss/p-gly) dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du client sur l’ordinateur du serveur</span><span class="sxs-lookup"><span data-stu-id="f69b9-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="f69b9-109">Un serveur protégé contrôle l’accès à ses services.</span><span class="sxs-lookup"><span data-stu-id="f69b9-109">A protected server controls access to its services.</span></span> <span data-ttu-id="f69b9-110">Windows fournit une prise en charge de la sécurité qui permet à un serveur d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f69b9-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="f69b9-111">Emprunter l’identité du contexte de [*sécurité*](/windows/desktop/SecGloss/s-gly)d’un client, ce qui amène le système à effectuer la plupart des contrôles d’accès et de [*privilège*](/windows/desktop/SecGloss/p-gly) sur le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du client plutôt que sur le serveur</span><span class="sxs-lookup"><span data-stu-id="f69b9-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="f69b9-112">Enregistrer un client sur l’ordinateur du serveur</span><span class="sxs-lookup"><span data-stu-id="f69b9-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="f69b9-113">Se connecter aux ressources réseau à l’aide du contexte de sécurité du client</span><span class="sxs-lookup"><span data-stu-id="f69b9-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="f69b9-114">Créer des [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly) pour protéger des objets privés</span><span class="sxs-lookup"><span data-stu-id="f69b9-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="f69b9-115">Déterminer si un descripteur de sécurité autorise l’accès à un client</span><span class="sxs-lookup"><span data-stu-id="f69b9-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="f69b9-116">Déterminer si un jeu de privilèges est activé dans le jeton d’un client</span><span class="sxs-lookup"><span data-stu-id="f69b9-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="f69b9-117">Générer des messages d’audit dans le journal des événements de sécurité pour enregistrer les tentatives d’accès par un client aux objets ou utiliser des privilèges</span><span class="sxs-lookup"><span data-stu-id="f69b9-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
