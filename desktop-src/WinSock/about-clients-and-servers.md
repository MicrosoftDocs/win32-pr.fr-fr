---
description: 'Il existe deux types distincts d’applications réseau de socket : serveur et client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: À propos des serveurs et des clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516249"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="bd1d6-103">À propos des serveurs et des clients</span><span class="sxs-lookup"><span data-stu-id="bd1d6-103">About Servers and Clients</span></span>

<span data-ttu-id="bd1d6-104">Il existe deux types distincts d’applications réseau de socket : serveur et client.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="bd1d6-105">Les serveurs et les clients ont des comportements différents ; par conséquent, le processus de création de ces éléments est différent.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="bd1d6-106">Ce qui suit est le modèle général pour la création d’un serveur et d’un client TCP/IP de streaming.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="bd1d6-107">Serveur</span><span class="sxs-lookup"><span data-stu-id="bd1d6-107">Server</span></span>

1.  <span data-ttu-id="bd1d6-108">Initialisez Winsock.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="bd1d6-109">Créer un Socket.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-109">Create a socket.</span></span>
3.  <span data-ttu-id="bd1d6-110">Liez le Socket.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-110">Bind the socket.</span></span>
4.  <span data-ttu-id="bd1d6-111">Écoute sur le socket pour un client.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="bd1d6-112">Accepter une connexion à partir d’un client.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="bd1d6-113">Recevoir et envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-113">Receive and send data.</span></span>
7.  <span data-ttu-id="bd1d6-114">Se déconnecter.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="bd1d6-115">Client</span><span class="sxs-lookup"><span data-stu-id="bd1d6-115">Client</span></span>

1.  <span data-ttu-id="bd1d6-116">Initialisez Winsock.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="bd1d6-117">Créer un Socket.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-117">Create a socket.</span></span>
3.  <span data-ttu-id="bd1d6-118">Connectez-vous au serveur.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-118">Connect to the server.</span></span>
4.  <span data-ttu-id="bd1d6-119">Envoyer et recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-119">Send and receive data.</span></span>
5.  <span data-ttu-id="bd1d6-120">Se déconnecter.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="bd1d6-121">Certaines étapes sont identiques pour un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="bd1d6-122">Ces étapes sont implémentées presque exactement de la même façon.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="bd1d6-123">Certaines étapes de ce guide sont spécifiques au type d’application en cours de création.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="bd1d6-124">Première étape : [création d’une application Winsock de base](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd1d6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd1d6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd1d6-126">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="bd1d6-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



