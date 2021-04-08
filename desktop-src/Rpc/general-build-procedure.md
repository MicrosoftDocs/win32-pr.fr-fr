---
title: Procédure de génération générale
description: Page de navigation pour le processus de création d’une application client/serveur à l’aide d’un appel de procédure distante (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029085"
---
# <a name="general-build-procedure"></a><span data-ttu-id="c1ec8-103">Procédure de génération générale</span><span class="sxs-lookup"><span data-stu-id="c1ec8-103">General Build Procedure</span></span>

<span data-ttu-id="c1ec8-104">Le processus de création d’une application client/serveur à l’aide de Microsoft RPC est le suivant :</span><span class="sxs-lookup"><span data-stu-id="c1ec8-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="c1ec8-105">Développez l’interface.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-105">Develop the interface.</span></span>
-   <span data-ttu-id="c1ec8-106">Développez le serveur qui implémente l’interface.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="c1ec8-107">Développez le client qui utilise l’interface.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="c1ec8-108">La figure suivante illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-108">The following figure illustrates these steps.</span></span>

![processus de création d’une application client-serveur à l’aide de Microsoft RPC](images/appdev.png)

<span data-ttu-id="c1ec8-110">Il est possible et courant de développer simultanément les applications client et serveur.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="c1ec8-111">Étant donné que les programmes client et serveur sont tous deux dépendants de l’interface, l’interface entre eux doit être développée avant le développement du client et du serveur, comme indiqué dans le diagramme précédent.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="c1ec8-112">Cette section décrit les étapes nécessaires à la création d’une application client/serveur avec RPC.</span><span class="sxs-lookup"><span data-stu-id="c1ec8-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="c1ec8-113">Les informations sont présentées dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c1ec8-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="c1ec8-114">Développement de l’interface</span><span class="sxs-lookup"><span data-stu-id="c1ec8-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="c1ec8-115">Développement du serveur</span><span class="sxs-lookup"><span data-stu-id="c1ec8-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="c1ec8-116">Développement du client</span><span class="sxs-lookup"><span data-stu-id="c1ec8-116">Developing the Client</span></span>](developing-the-client.md)

 

 




