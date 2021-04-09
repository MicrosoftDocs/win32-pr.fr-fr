---
description: Décrit les fonctionnalités d’un redirecteur réseau.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirecteurs réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868914"
---
# <a name="network-redirectors"></a><span data-ttu-id="0e07a-103">Redirecteurs réseau</span><span class="sxs-lookup"><span data-stu-id="0e07a-103">Network Redirectors</span></span>

<span data-ttu-id="0e07a-104">Un redirecteur réseau est un pilote de système de fichiers (ou FSD) qui fonctionne de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="0e07a-104">A network redirector is a file system driver (or FSD) that functions in the following manner:</span></span>

-   <span data-ttu-id="0e07a-105">En tant que client dans le cadre d’une opération d’e/s réseau en envoyant des demandes d’e/s aux serveurs et en traitant les réponses des serveurs.</span><span class="sxs-lookup"><span data-stu-id="0e07a-105">As a client in a network I/O operation by sending I/O requests to servers and processing the responses from the servers.</span></span>
-   <span data-ttu-id="0e07a-106">En tant que serveur dans le cadre d’une opération d’e/s réseau en recevant des demandes d’e/s des serveurs et en traitant les demandes.</span><span class="sxs-lookup"><span data-stu-id="0e07a-106">As a server in a network I/O operation by receiving I/O requests from servers and processing the requests.</span></span>

<span data-ttu-id="0e07a-107">Il effectue toute l’interaction de bas niveau avec le serveur pour résoudre le nom de fichier fourni par l’application avec l’emplacement de la ressource sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="0e07a-107">It performs all of the low-level interaction with the server in resolving the file name provided by the application with the location of the resource on the remote server.</span></span> <span data-ttu-id="0e07a-108">De cette façon, le redirecteur permet à l’application d’accéder aux ressources sur les serveurs distants et de les manipuler comme si elles se trouvaient sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0e07a-108">In this way, the redirector enables the application to access and manipulate resources on remote servers as if they were located on the local machine.</span></span>

<span data-ttu-id="0e07a-109">Les redirecteurs fonctionnent entièrement en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="0e07a-109">Redirectors operate entirely within kernel mode.</span></span> <span data-ttu-id="0e07a-110">Cela offre les avantages suivants en matière de performances par rapport aux alternatives en mode utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0e07a-110">This provides the following performance advantages over user-mode alternatives:</span></span>

-   <span data-ttu-id="0e07a-111">Il peut interagir avec les FSDs en mode noyau s’exécutant sur le serveur, tels que le serveur FSD, sans nécessiter de commutateurs de contexte de mode noyau à utilisateur et de mode utilisateur à noyau.</span><span class="sxs-lookup"><span data-stu-id="0e07a-111">It can interact with kernel-mode FSDs running on the server, such as the server FSD, without the need for user-to-kernel mode and kernel-to-user mode context switches.</span></span>
-   <span data-ttu-id="0e07a-112">Il peut interagir en mode noyau avec le gestionnaire de cache sur le serveur pour mettre en cache les données d’e/s envoyées par le gestionnaire de cache du serveur sur le client.</span><span class="sxs-lookup"><span data-stu-id="0e07a-112">It can interact in kernel mode with the cache manager on the server to cache I/O data that the server cache manager sends on the client.</span></span>
-   <span data-ttu-id="0e07a-113">Les fonctions d’API personnalisées pour les demandes d’e/s distantes et les modifications apportées aux fonctions d’e/s de fichier standard pour fournir cette fonctionnalité ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0e07a-113">API functions custom-made for remote I/O requests, and changes to the standard file I/O functions to provide this functionality, are not necessary.</span></span>

 

 



