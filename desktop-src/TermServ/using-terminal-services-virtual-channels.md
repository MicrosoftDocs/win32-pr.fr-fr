---
title: Utilisation de Services Bureau à distance canaux virtuels
description: Pour implémenter un canal virtuel, vous fournissez les modules serveur et client de l’application d’un canal virtuel.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672034"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="80c96-103">Utilisation de Services Bureau à distance canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="80c96-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="80c96-104">Pour implémenter un canal virtuel, vous fournissez les modules serveur et client de l’application d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="80c96-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="80c96-105">Le module de serveur peut être une application en mode utilisateur ou un pilote en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="80c96-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="80c96-106">Le module client doit être une DLL.</span><span class="sxs-lookup"><span data-stu-id="80c96-106">The client module must be a DLL.</span></span>

<span data-ttu-id="80c96-107">Pour obtenir une description de ces modules, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="80c96-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="80c96-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="80c96-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="80c96-109">Application de serveur de canal virtuel</span><span class="sxs-lookup"><span data-stu-id="80c96-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="80c96-110">Le module de serveur d’une application qui utilise des canaux virtuels doit être une application en mode utilisateur s’exécutant dans une session cliente sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="80c96-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="80c96-111">Notez que vous devez fournir une méthode pour démarrer l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="80c96-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="80c96-112">DLL du client du canal virtuel</span><span class="sxs-lookup"><span data-stu-id="80c96-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="80c96-113">Le client d’une application de canaux virtuels est une DLL qui est chargée pendant l’initialisation Services Bureau à distance sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="80c96-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="80c96-114">La DLL doit être inscrite sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="80c96-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="80c96-115">Inscription du client du canal virtuel</span><span class="sxs-lookup"><span data-stu-id="80c96-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="80c96-116">Vous devez stocker le nom de la DLL cliente dans le registre.</span><span class="sxs-lookup"><span data-stu-id="80c96-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="80c96-117">Canaux virtuels persistants de contrôle à distance</span><span class="sxs-lookup"><span data-stu-id="80c96-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="80c96-118">Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client.</span><span class="sxs-lookup"><span data-stu-id="80c96-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="80c96-119">Les données continueront à être transmises et reçues via ce canal.</span><span class="sxs-lookup"><span data-stu-id="80c96-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="80c96-120">Canaux virtuels dynamiques</span><span class="sxs-lookup"><span data-stu-id="80c96-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="80c96-121">Les API de canal virtuel dynamique (DVC) étendent les API de canal virtuel existantes pour Services Bureau à distance, appelées API de canal virtuel statique (SVC).</span><span class="sxs-lookup"><span data-stu-id="80c96-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="80c96-122">Si vous avez activé l’application d’un canal virtuel dans votre déploiement Services Bureau à distance, vous pouvez également rendre l’application disponible pour les ordinateurs clients qui accèdent au serveur hôte de session Bureau à distance à l’aide du contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="80c96-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="80c96-123">Pour plus d’informations, consultez [utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="80c96-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




