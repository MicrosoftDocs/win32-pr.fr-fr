---
title: Services Bureau à distance des canaux virtuels
description: Les canaux virtuels sont des extensions logicielles qui peuvent être utilisées pour ajouter des améliorations fonctionnelles à une application Services Bureau à distance.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309890"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="7e0e3-103">Services Bureau à distance des canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="7e0e3-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="7e0e3-104">Les *canaux virtuels* sont des extensions logicielles qui peuvent être utilisées pour ajouter des améliorations fonctionnelles à une application services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="7e0e3-105">Parmi les exemples d’améliorations fonctionnelles, citons notamment la prise en charge de types spéciaux de matériel, de son ou d’autres ajouts à la fonctionnalité de base fournie par le Services Bureau à distance [protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md) (RDP).</span><span class="sxs-lookup"><span data-stu-id="7e0e3-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="7e0e3-106">Le protocole RDP offre une gestion multiplexée de plusieurs canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7e0e3-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7e0e3-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7e0e3-108">Utilisation de Services Bureau à distance canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="7e0e3-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="7e0e3-109">Pour implémenter un canal virtuel, vous fournissez les modules serveur et client de l’application d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="7e0e3-110">Référence des canaux virtuels dynamiques</span><span class="sxs-lookup"><span data-stu-id="7e0e3-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="7e0e3-111">Les interfaces clientes de canal virtuel dynamique (DVC) sont prises en charge par Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="7e0e3-112">Informations de référence sur les canaux virtuels Graphics</span><span class="sxs-lookup"><span data-stu-id="7e0e3-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="7e0e3-113">Les informations de référence sur les canaux virtuels Graphics contiennent des éléments de programmation qui vous permettent de créer un canal graphique virtuel.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="7e0e3-114">Une application de canal virtuel a deux parties : un module client et un module serveur.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="7e0e3-115">Le module de serveur est un programme exécutable s’exécutant sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="7e0e3-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="7e0e3-116">Le module client est une DLL qui doit être chargée en mémoire sur l’ordinateur client lors de l’exécution du programme client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="7e0e3-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="7e0e3-117">Les canaux virtuels peuvent ajouter des améliorations fonctionnelles à un client Connexion Bureau à distance (RDC), indépendamment du protocole RDP.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="7e0e3-118">Avec la prise en charge des canaux virtuels, de nouvelles fonctionnalités peuvent être ajoutées sans avoir à mettre à jour le logiciel client ou serveur, ni le protocole RDP.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="7e0e3-119">Quatre grandes classes d’utilisateurs de canaux virtuels ont été identifiées :</span><span class="sxs-lookup"><span data-stu-id="7e0e3-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="7e0e3-120">Pilotes généraux en mode noyau, tels que les pilotes série ou d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="7e0e3-121">Redirection du système de fichiers (il s’agit simplement d’un cas particulier d’un pilote en mode noyau général).</span><span class="sxs-lookup"><span data-stu-id="7e0e3-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="7e0e3-122">Applications en mode utilisateur, par exemple, couper-coller à distance.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="7e0e3-123">Périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-123">Audio devices.</span></span>

<span data-ttu-id="7e0e3-124">Pour plus d’informations, consultez [utilisation de services Bureau à distance canaux virtuels](using-terminal-services-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="7e0e3-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="7e0e3-125">Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez rendre l’application accessible aux ordinateurs clients qui accèdent au serveur hôte de session Bureau à distance à l’aide de l’Bureau à distance contrôle Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="7e0e3-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="7e0e3-126">Pour plus d’informations, consultez [canaux virtuels scriptables](scriptable-virtual-channels.md) et [utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="7e0e3-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




