---
description: Composants homologues Windows pour voisinage immédiat
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Composants homologues Windows pour voisinage immédiat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952022"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="9bf1c-103">Composants homologues Windows pour voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="9bf1c-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="9bf1c-104">Dans l’exécutable de mise en réseau d’homologue Windows (P2phost.exe) principal, l' [architecture voisinage immédiat](people-near-me-architecture.md) utilise les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="9bf1c-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="9bf1c-105">Voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="9bf1c-105">People Near Me</span></span>

<span data-ttu-id="9bf1c-106">Le composant voisinage immédiat (PNM) initie la découverte à l’aide de la découverte de services Web sur le sous-réseau local pour les noms d’utilisateur des ordinateurs autorisés à PNM.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="9bf1c-107">Éditeur voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="9bf1c-107">People Near Me Publisher</span></span>

<span data-ttu-id="9bf1c-108">Le composant du serveur de publication voisinage immédiat publie les pseudos des utilisateurs connectés pour indiquer la disponibilité à d’autres ordinateurs à l’aide de PNM sur le sous-réseau local.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="9bf1c-109">L’utilisateur connecté doit choisir de publier son surnom avant qu’il ne soit publié.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="9bf1c-110">Le surnom est publié sur le sous-réseau à l’aide de la découverte de services Web.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="9bf1c-111">En outre, les objets et les applications peuvent également être publiés.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="9bf1c-112">Toutefois, l’utilisateur doit spécifier la publication de l’objet et de l’application pour les portées «**People Near me**» ou «**All**».</span><span class="sxs-lookup"><span data-stu-id="9bf1c-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="9bf1c-113">Énumérateur voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="9bf1c-113">People Near Me Enumerator</span></span>

<span data-ttu-id="9bf1c-114">Le composant énumérateur voisinage immédiat énumère la liste des utilisateurs sur le sous-réseau local.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="9bf1c-115">À l’aide de cette liste, la découverte de services Web envoie une requête de multidiffusion et reçoit les réponses.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="9bf1c-116">Une fois la liste des surnoms obtenue, une application peut utiliser l’API pour récupérer plus de données publiées par l’utilisateur (qui est chiffré à l’aide de [Schannel](windows-vista-components-for-people-near-me.md)), telles que la liste des applications inscrites et les objets en cours de publication.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="9bf1c-117">Le processus de recherche et d’énumération ne se produit pas automatiquement, mais doit être explicitement initié par un utilisateur ou une application en se connectant à PNM.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="9bf1c-118">Les résultats de la recherche sont la liste des diminutifs d’autres utilisateurs sur le même sous-réseau qui publient leurs surnoms à l’aide de l’API PNM.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="9bf1c-119">Gestionnaire de publication</span><span class="sxs-lookup"><span data-stu-id="9bf1c-119">Publication Manager</span></span>

<span data-ttu-id="9bf1c-120">Le composant Gestionnaire de publication est responsable de la publication des mises à jour de la présence, de l’application ou des objets sur les contacts ou les personnes proches de l’abonnement ou de l’interrogation des données.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="9bf1c-121">Signalisation d’homologue</span><span class="sxs-lookup"><span data-stu-id="9bf1c-121">Peer Signaling</span></span>

<span data-ttu-id="9bf1c-122">Le composant de signalement d’homologue gère la création de connexions entre homologues pour échanger des données.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="9bf1c-123">Pour voisinage immédiat, la signalisation d’homologue est utilisée lorsqu’un utilisateur ou une application envoie la requête de monodiffusion à un ordinateur spécifique pour sa clé publique, ses applications et ses objets.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="9bf1c-124">Recevoir le gestionnaire d’invitation/UX</span><span class="sxs-lookup"><span data-stu-id="9bf1c-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="9bf1c-125">Le composant Gestionnaire d’invitation de réception/UX reçoit une invitation entrante d’une autre personne, invite l’utilisateur à déterminer s’il souhaite lancer l’application associée à l’invitation, puis lance l’application en fonction de l’utilisateur qui accepte l’invitation.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="9bf1c-126">Une invitation est un message d’une autre personne qui lance l’activité de collaboration à l’aide d’une application spécifique installée sur les ordinateurs des utilisateurs et publiée par l’utilisateur invité.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="9bf1c-127">Sécurité de l’homologue</span><span class="sxs-lookup"><span data-stu-id="9bf1c-127">Peer Security</span></span>

<span data-ttu-id="9bf1c-128">Lorsque la présence, l’application et l’objet sont envoyés, les informations sont chiffrées à l’aide d’un canal SSL ([Schannel](windows-vista-components-for-people-near-me.md)).</span><span class="sxs-lookup"><span data-stu-id="9bf1c-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="9bf1c-129">L’ordinateur initiateur utilise la clé publique de l’ordinateur invité pour négocier une clé secrète utilisée pour chiffrer les données ultérieures envoyées entre les deux pairs.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



