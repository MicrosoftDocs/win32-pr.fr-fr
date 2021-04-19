---
title: Services Bureau à distance (Services Bureau à distance)
description: Les services Bureau à distance Microsoft sont des logiciels d’accès aux ordinateurs distants qui prennent en charge l’accès Bureau à distance. Services Bureau à distance connecte plusieurs clients à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance
- Services Bureau à distance Services Bureau à distance, page d’hébergement
- Services Terminal Server voir Services Bureau à distance Services Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510926"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="e164d-107">Services Bureau à distance (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="e164d-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="e164d-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="e164d-108">Purpose</span></span>

<span data-ttu-id="e164d-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 avec Services Bureau à distance (anciennement services Terminal Server) permettent à un serveur d’héberger plusieurs sessions clientes simultanées.</span><span class="sxs-lookup"><span data-stu-id="e164d-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="e164d-110">Bureau à distance utilise la technologie Services Bureau à distance pour permettre l’exécution à distance d’une seule session.</span><span class="sxs-lookup"><span data-stu-id="e164d-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="e164d-111">Un utilisateur peut se connecter à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement appelé serveur Terminal Server) à l’aide du logiciel client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="e164d-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="e164d-112">Le Connexion Bureau à distance par le Web étend la technologie Services Bureau à distance au Web.</span><span class="sxs-lookup"><span data-stu-id="e164d-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="e164d-113">Cette rubrique est destinée aux développeurs de logiciels.</span><span class="sxs-lookup"><span data-stu-id="e164d-113">This topic is for software developers.</span></span> <span data-ttu-id="e164d-114">Si vous recherchez des informations sur l’utilisateur pour les connexions Bureau à distance, consultez [Connexion Bureau à distance : Forum aux questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="e164d-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="e164d-115">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="e164d-115">Where applicable</span></span>

<span data-ttu-id="e164d-116">Un client Connexion Bureau à distance (RDC) peut exister sous différentes formes.</span><span class="sxs-lookup"><span data-stu-id="e164d-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="e164d-117">Les périphériques matériels clients légers qui exécutent un système d’exploitation Windows intégré peuvent exécuter le logiciel client RDC pour se connecter à un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e164d-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="e164d-118">Les ordinateurs Windows, Macintosh ou UNIX peuvent exécuter le logiciel client RDC pour se connecter à un serveur hôte de session Bureau à distance pour afficher des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="e164d-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="e164d-119">Cette combinaison de clients RDC permet d’accéder aux applications Windows à partir de pratiquement n’importe quel système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e164d-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e164d-120">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="e164d-120">Developer audience</span></span>

<span data-ttu-id="e164d-121">Les développeurs qui utilisent Services Bureau à distance doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation basé sur Windows.</span><span class="sxs-lookup"><span data-stu-id="e164d-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="e164d-122">Vous devez vous familiariser avec l’architecture client/serveur.</span><span class="sxs-lookup"><span data-stu-id="e164d-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="e164d-123">Le Connexion Bureau à distance par le Web comprend des interfaces scriptables pour créer et déployer des canaux virtuels scriptables dans des applications Web Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e164d-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e164d-124">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="e164d-124">Run-time requirements</span></span>

<span data-ttu-id="e164d-125">Les applications qui utilisent Services Bureau à distance requièrent Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e164d-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="e164d-126">Pour utiliser Connexion Bureau à distance par le Web fonctionnalité, l’application cliente Services Bureau à distance nécessite Internet Explorer et une connexion à la World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="e164d-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="e164d-127">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="e164d-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e164d-128">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e164d-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e164d-129">Contrôle ActiveX Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="e164d-130">Décrit comment utiliser le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e164d-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-131">API du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="e164d-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="e164d-132">Vous utilisez l’API du fournisseur protocole RDP (Remote Desktop Protocol) pour créer un protocole pour assurer la communication entre le service Services Bureau à distance et plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="e164d-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-133">Services Bureau à distance des canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="e164d-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="e164d-134">Les *canaux virtuels* sont des extensions logicielles qui peuvent être utilisées pour ajouter des améliorations fonctionnelles à une application services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e164d-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-135">API de redirection multimédia RemoteFX</span><span class="sxs-lookup"><span data-stu-id="e164d-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="e164d-136">L’API de redirection multimédia RemoteFX est utilisée dans une session Bureau à distance pour identifier les zones du serveur qui affichent le contenu à variation rapide, tel que la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e164d-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="e164d-137">Ce contenu peut ensuite être encodé en vidéo et envoyé au client dans un format encodé.</span><span class="sxs-lookup"><span data-stu-id="e164d-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-138">API du client Connexion Bureau à distance Broker</span><span class="sxs-lookup"><span data-stu-id="e164d-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="e164d-139">Décrit comment utiliser l’API cliente Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="e164d-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-140">Informations de référence sur l’API agent des tâches du bureau personnel</span><span class="sxs-lookup"><span data-stu-id="e164d-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="e164d-141">L’API agent de tâche de bureau personnel est utilisée pour gérer les mises à jour planifiées d’un bureau virtuel personnel.</span><span class="sxs-lookup"><span data-stu-id="e164d-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-142">À propos de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="e164d-143">Services Bureau à distance (anciennement services Terminal Server) offre des fonctionnalités similaires à celles d’un environnement de type terminal, d’un ordinateur hôte centralisé ou d’un macroordinateur dans lequel plusieurs terminaux se connectent à un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="e164d-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-144">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="e164d-145">Le fournisseur Bureau à distance Management Services (RDMS) gère les environnements VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="e164d-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-146">Référence Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="e164d-147">Documentation des méthodes de propriété que vous pouvez utiliser pour examiner et configurer Services Bureau à distance propriétés de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e164d-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="e164d-148">Services Bureau à distance les fonctions, structures et Connexion Bureau à distance par le Web les interfaces scriptables sont également documentées.</span><span class="sxs-lookup"><span data-stu-id="e164d-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-149">Touches de raccourci Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="e164d-150">Liste des touches de raccourci de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e164d-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-151">Fournisseur WMI Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="e164d-152">Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e164d-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="e164d-153">Utilisation de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="e164d-154">Comment programmer dans l’environnement Services Bureau à distance et comment étendre la technologie Services Bureau à distance (anciennement appelée services Terminal Server) au Web à l’aide de Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="e164d-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e164d-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e164d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e164d-156">Les services Terminal Server sont désormais Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e164d-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




