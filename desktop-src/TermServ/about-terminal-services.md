---
title: À propos de Services Bureau à distance
description: Services Bureau à distance (anciennement services Terminal Server) offre des fonctionnalités similaires à celles d’un environnement de type terminal, d’un ordinateur hôte centralisé ou d’un macroordinateur dans lequel plusieurs terminaux se connectent à un ordinateur hôte.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106522627"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="f2d0b-104">À propos de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-104">About Remote Desktop Services</span></span>

<span data-ttu-id="f2d0b-105">Services Bureau à distance (anciennement services Terminal Server) offre des fonctionnalités similaires à celles d’un environnement de type terminal, d’un ordinateur hôte centralisé ou d’un macroordinateur dans lequel plusieurs terminaux se connectent à un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="f2d0b-106">Chaque terminal fournit un canal d’entrée et de sortie entre un utilisateur et l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="f2d0b-107">Un utilisateur peut ouvrir une session sur un terminal, puis exécuter des applications sur l’ordinateur hôte, accéder à des fichiers, des bases de données, des ressources réseau, etc.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="f2d0b-108">Chaque session de terminal est indépendante, avec le système d’exploitation hôte qui gère les conflits entre plusieurs utilisateurs qui ont des ressources partagées.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="f2d0b-109">La principale différence entre les Services Bureau à distance et l’environnement de macroordinateur traditionnel est que les terminaux passifs dans un environnement de macroordinateur fournissent uniquement une entrée et une sortie basées sur des caractères.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="f2d0b-110">Un client ou un émulateur Connexion Bureau à distance (RDC) fournit une interface utilisateur graphique complète comprenant un bureau du système d’exploitation Windows et la prise en charge d’un large éventail de périphériques d’entrée, tels qu’un clavier et une souris.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="f2d0b-111">Dans l’environnement de Services Bureau à distance, une application s’exécute entièrement sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement appelé Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="f2d0b-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="f2d0b-112">Le client RDC n’effectue aucun traitement local des logiciels d’application.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="f2d0b-113">Le serveur transmet l’interface utilisateur graphique au client.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="f2d0b-114">Le client transmet à nouveau l’entrée de l’utilisateur au serveur.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="f2d0b-115">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2d0b-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f2d0b-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f2d0b-117">Modifier la valeur par défaut de la redirection de périphérique</span><span class="sxs-lookup"><span data-stu-id="f2d0b-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="f2d0b-118">Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-119">Protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="f2d0b-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="f2d0b-120">Le protocole RDP (Bureau à distance Microsoft Protocol) fournit des fonctionnalités d’affichage et d’entrée à distance sur les connexions réseau pour les applications Windows exécutées sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-121">API Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="f2d0b-122">L’API Services Bureau à distance est surtout utile pour les applications client/serveur et les applications pour l’administration des Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-123">Applications de gestion de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="f2d0b-124">Décrit les applications de gestion prises en charge par Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-125">Instructions de programmation Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="f2d0b-126">Rubriques qui fournissent des instructions pour le développement d’applications dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-127">Sessions Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="f2d0b-128">Étant donné que chaque connexion à un client Connexion Bureau à distance (RDC) reçoit un ID de session distinct, l’expérience utilisateur est semblable à la connexion à plusieurs ordinateurs en même temps. par exemple, un ordinateur de bureau et un ordinateur privé.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-129">Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="f2d0b-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="f2d0b-130">Décrit comment installer un Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-131">Ressources sur un serveur hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="f2d0b-132">Plusieurs utilisateurs peuvent se connecter simultanément à un seul serveur hôte de session Bureau à distance, en partageant les ressources matérielles et logicielles du serveur.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="f2d0b-133">Nouveautés de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="f2d0b-134">Rubriques qui décrivent les modifications apportées à chaque version de l’API Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f2d0b-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f2d0b-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2d0b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2d0b-136">Se connecter à un autre ordinateur à l’aide de Connexion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f2d0b-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




