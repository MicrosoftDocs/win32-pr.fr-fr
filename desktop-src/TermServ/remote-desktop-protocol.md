---
title: Protocole RDP (Remote Desktop Protocol)
description: Le protocole RDP (Bureau à distance Microsoft Protocol) fournit des fonctionnalités d’affichage et d’entrée à distance sur les connexions réseau pour les applications Windows exécutées sur un serveur.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance protocole RDP (Remote Desktop Protocol) (RDP)
- RDP (voir protocole RDP (Remote Desktop Protocol))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510886"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="032b2-105">Protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="032b2-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="032b2-106">Le protocole RDP (Bureau à distance Microsoft Protocol) fournit des fonctionnalités d’affichage et d’entrée à distance sur les connexions réseau pour les applications Windows exécutées sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="032b2-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="032b2-107">RDP est conçu pour prendre en charge différents types de topologies de réseau et de plusieurs protocoles LAN.</span><span class="sxs-lookup"><span data-stu-id="032b2-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="032b2-108">Cette rubrique est destinée aux développeurs de logiciels.</span><span class="sxs-lookup"><span data-stu-id="032b2-108">This topic is for software developers.</span></span> <span data-ttu-id="032b2-109">Si vous recherchez des informations utilisateur pour Bureau à distance, consultez [prise en charge de Windows](https://windows.microsoft.com/windows/support#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="032b2-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="032b2-110">Si vous recherchez des informations destinées aux professionnels de l’informatique pour Bureau à distance, consultez [services Bureau à distance sur TechNet](/windows/deployment/deploy-whats-new).</span><span class="sxs-lookup"><span data-stu-id="032b2-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="032b2-111">Architecture de base</span><span class="sxs-lookup"><span data-stu-id="032b2-111">Basic Architecture</span></span>

<span data-ttu-id="032b2-112">RDP est basé sur et sur une extension de la famille de protocoles ITU T. 120.</span><span class="sxs-lookup"><span data-stu-id="032b2-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="032b2-113">RDP est un protocole prenant en charge plusieurs canaux qui autorise des canaux virtuels distincts pour transporter les données de communication et de présentation des appareils à partir du serveur, ainsi que des données de clavier et de souris du client chiffrées.</span><span class="sxs-lookup"><span data-stu-id="032b2-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="032b2-114">RDP fournit une base extensible et prend en charge jusqu’à 64 000 canaux distincts pour la transmission de données et les dispositions pour la transmission multipoint.</span><span class="sxs-lookup"><span data-stu-id="032b2-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="032b2-115">Sur le serveur, RDP utilise son propre pilote vidéo pour restituer la sortie d’affichage en construisant les informations de rendu dans des paquets réseau à l’aide du protocole RDP et en les envoyant au client via le réseau.</span><span class="sxs-lookup"><span data-stu-id="032b2-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="032b2-116">Sur le client, le protocole RDP reçoit les données de rendu et interprète les paquets dans les appels d’API GDI (Graphics Device Interface) Microsoft Windows correspondants.</span><span class="sxs-lookup"><span data-stu-id="032b2-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="032b2-117">Pour le chemin d’entrée, les événements de souris et de clavier du client sont redirigés du client vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="032b2-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="032b2-118">Sur le serveur, RDP utilise son propre pilote de clavier et de souris pour recevoir ces événements de clavier et de souris.</span><span class="sxs-lookup"><span data-stu-id="032b2-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="032b2-119">Dans une session Bureau à distance, toutes les variables d’environnement (par exemple, les variables déterminant la profondeur de couleur et l’activation et la désactivation du papier peint) sont déterminées par les paramètres de connexion RCP-Tcp.</span><span class="sxs-lookup"><span data-stu-id="032b2-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="032b2-120">Cela s’applique à toutes les fonctions et méthodes qui définissent les variables d’environnement dans la [référence connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md) et l' [interface du fournisseur WMI services Bureau à distance](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="032b2-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="032b2-121">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="032b2-121">Features</span></span>

<span data-ttu-id="032b2-122">Microsoft RDP comprend les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="032b2-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="032b2-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Chiffre</span><span class="sxs-lookup"><span data-stu-id="032b2-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="032b2-124">RDP utilise le chiffrement RC4 de RSA Security, un chiffrement de flux conçu pour chiffrer efficacement de petites quantités de données.</span><span class="sxs-lookup"><span data-stu-id="032b2-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="032b2-125">RC4 est conçu pour sécuriser les communications sur les réseaux.</span><span class="sxs-lookup"><span data-stu-id="032b2-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="032b2-126">Les administrateurs peuvent choisir de chiffrer les données à l’aide d’une clé 56 ou 128 bits.</span><span class="sxs-lookup"><span data-stu-id="032b2-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Fonctionnalités de réduction de bande passante</span><span class="sxs-lookup"><span data-stu-id="032b2-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="032b2-128">RDP prend en charge différents mécanismes pour réduire la quantité de données transmises sur une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="032b2-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="032b2-129">Les mécanismes incluent la compression des données, la mise en cache persistante des bitmaps et la mise en cache des glyphes et des fragments dans la RAM.</span><span class="sxs-lookup"><span data-stu-id="032b2-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="032b2-130">Le cache de bitmaps persistant peut améliorer considérablement les performances par rapport aux connexions à faible bande passante, en particulier lors de l’exécution d’applications qui utilisent intensivement des bitmaps de grande taille.</span><span class="sxs-lookup"><span data-stu-id="032b2-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Déconnexion itinérante</span><span class="sxs-lookup"><span data-stu-id="032b2-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="032b2-132">Un utilisateur peut se déconnecter manuellement d’une session Bureau à distance sans fermer la session.</span><span class="sxs-lookup"><span data-stu-id="032b2-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="032b2-133">L’utilisateur est automatiquement reconnecté à sa session déconnectée lorsqu’il se reconnecte au système à partir du même appareil ou d’un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="032b2-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="032b2-134">Lorsque la session d’un utilisateur se termine de façon inattendue par une défaillance du réseau ou du client, l’utilisateur est déconnecté, mais pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="032b2-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mappage du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="032b2-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="032b2-136">Les utilisateurs peuvent supprimer, copier et coller du texte et des graphiques entre les applications qui s’exécutent sur l’ordinateur local et celles qui s’exécutent dans une session Bureau à distance, et entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="032b2-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirection d’impression</span><span class="sxs-lookup"><span data-stu-id="032b2-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="032b2-138">Les applications qui s’exécutent dans une session Bureau à distance peuvent imprimer sur une imprimante connectée à l’appareil client.</span><span class="sxs-lookup"><span data-stu-id="032b2-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="032b2-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="032b2-140">Grâce à l’architecture de canal virtuel RDP, les applications existantes peuvent être augmentées et de nouvelles applications peuvent être développées pour ajouter des fonctionnalités qui nécessitent des communications entre le périphérique client et une application s’exécutant dans une session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="032b2-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Contrôle à distance</span><span class="sxs-lookup"><span data-stu-id="032b2-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="032b2-142">Le personnel de support informatique peut afficher et contrôler une session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="032b2-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="032b2-143">Partager des entrées et afficher des graphiques entre deux sessions Bureau à distance permet à une personne du support de diagnostiquer et de résoudre les problèmes à distance.</span><span class="sxs-lookup"><span data-stu-id="032b2-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="032b2-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Équilibrage de la charge réseau</span><span class="sxs-lookup"><span data-stu-id="032b2-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="032b2-145">RDP tire parti de l’équilibrage de la charge réseau (NLB), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="032b2-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="032b2-146">En outre, le protocole RDP contient les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="032b2-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="032b2-147">Prise en charge des couleurs 24 bits.</span><span class="sxs-lookup"><span data-stu-id="032b2-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="032b2-148">Amélioration des performances par rapport aux connexions d’accès à distance à faible vitesse via une bande passante réduite.</span><span class="sxs-lookup"><span data-stu-id="032b2-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="032b2-149">Authentification par carte à puce via Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="032b2-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="032b2-150">Connexion au clavier.</span><span class="sxs-lookup"><span data-stu-id="032b2-150">Keyboard hooking.</span></span> <span data-ttu-id="032b2-151">Possibilité de regrouper des combinaisons de touches Windows spéciales, en mode plein écran, sur l’ordinateur local ou sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="032b2-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="032b2-152">Le son, le lecteur, le port et la redirection d’imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="032b2-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="032b2-153">Les sons qui se produisent sur l’ordinateur distant peuvent être audibles sur l’ordinateur client qui exécute le client RDC, et les lecteurs clients locaux sont visibles par la session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="032b2-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 