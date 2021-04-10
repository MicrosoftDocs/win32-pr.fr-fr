---
title: Modèle d’exécution
description: Modèle d’exécution
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modèle d’exécution
- modèle d’exécution OpenGL
- OpenGL, modèle client/serveur
- modèle client/serveur OpenGL
- OpenGL, transparent pour le réseau
- framebuffers, modèle d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940225"
---
# <a name="execution-model"></a><span data-ttu-id="67d75-109">Modèle d’exécution</span><span class="sxs-lookup"><span data-stu-id="67d75-109">Execution Model</span></span>

<span data-ttu-id="67d75-110">Le modèle d’interprétation des commandes OpenGL est client/serveur.</span><span class="sxs-lookup"><span data-stu-id="67d75-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="67d75-111">Le code d’application (le client) émet des commandes qui sont interprétées et traitées par OpenGL (le serveur).</span><span class="sxs-lookup"><span data-stu-id="67d75-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="67d75-112">Le serveur peut s’exécuter ou non sur le même ordinateur que le client.</span><span class="sxs-lookup"><span data-stu-id="67d75-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="67d75-113">Dans ce sens, OpenGL est transparent pour le réseau.</span><span class="sxs-lookup"><span data-stu-id="67d75-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="67d75-114">Un serveur peut gérer plusieurs contextes OpenGL, chacun d’eux étant un État OpenGL encapsulé.</span><span class="sxs-lookup"><span data-stu-id="67d75-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="67d75-115">Un client peut se connecter à l’un de ces contextes.</span><span class="sxs-lookup"><span data-stu-id="67d75-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="67d75-116">Le protocole réseau requis peut être implémenté en augmentant un protocole existant (tel que celui du système de fenêtre X) ou en utilisant un protocole indépendant.</span><span class="sxs-lookup"><span data-stu-id="67d75-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="67d75-117">Aucune commande OpenGL n’est fournie pour obtenir une entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67d75-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="67d75-118">Le système de fenêtre qui alloue des ressources trame contrôle finalement les effets des commandes OpenGL sur le trame.</span><span class="sxs-lookup"><span data-stu-id="67d75-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="67d75-119">Le système de fenêtre :</span><span class="sxs-lookup"><span data-stu-id="67d75-119">The window system:</span></span>

-   <span data-ttu-id="67d75-120">Détermine les parties de l’trame OpenGL qui peuvent accéder à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="67d75-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="67d75-121">Communique avec OpenGL sur la structure de ces parties.</span><span class="sxs-lookup"><span data-stu-id="67d75-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="67d75-122">Par conséquent, il n’existe aucune commande OpenGL pour configurer trame ou initialiser OpenGL.</span><span class="sxs-lookup"><span data-stu-id="67d75-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="67d75-123">La configuration de la mémoire tampon de frame est effectuée en dehors d’OpenGL conjointement avec le système Windows. L’initialisation OpenGL a lieu lorsque le système de fenêtres alloue une fenêtre pour le rendu OpenGL.</span><span class="sxs-lookup"><span data-stu-id="67d75-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




