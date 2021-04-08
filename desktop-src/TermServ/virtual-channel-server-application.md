---
title: Application de serveur de canal virtuel
description: Le module de serveur d’une application qui utilise des canaux virtuels doit être une application en mode utilisateur s’exécutant dans une session cliente sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Notez que vous devez fournir une méthode pour démarrer l’application serveur.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673809"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="538c9-104">Application de serveur de canal virtuel</span><span class="sxs-lookup"><span data-stu-id="538c9-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="538c9-105">Le module de serveur d’une application qui utilise des canaux virtuels doit être une application en mode utilisateur s’exécutant dans une session cliente sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="538c9-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="538c9-106">Notez que vous devez fournir une méthode pour démarrer l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="538c9-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="538c9-107">Pour ce faire, vous pouvez procéder de plusieurs façons : par exemple, vous pouvez utiliser un script d’ouverture de session ou un programme ou un script dans le dossier de démarrage.</span><span class="sxs-lookup"><span data-stu-id="538c9-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="538c9-108">Les utilisateurs peuvent également lancer l’application.</span><span class="sxs-lookup"><span data-stu-id="538c9-108">Users could also launch the application.</span></span>

<span data-ttu-id="538c9-109">Vous devez stocker le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé sous l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="538c9-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="538c9-110">**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** de contrôle CurrentControlSet du système de l’ordinateur local Terminal Server</span><span class="sxs-lookup"><span data-stu-id="538c9-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="538c9-111">Pour plus d’informations sur la sous-clé, consultez [surveillance des connexions de session et des déconnexions](monitoring-session-connections-and-disconnections.md).</span><span class="sxs-lookup"><span data-stu-id="538c9-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="538c9-112">L’application serveur peut appeler la fonction [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) pour ouvrir un handle vers un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="538c9-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="538c9-113">L’application peut ensuite utiliser le descripteur dans l’une des fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="538c9-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="538c9-114">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="538c9-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="538c9-115">Ferme un handle de canal virtuel ouvert.</span><span class="sxs-lookup"><span data-stu-id="538c9-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="538c9-116">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="538c9-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="538c9-117">Supprime toutes les données d’entrée mises en file d’attente envoyées du client au serveur sur un canal virtuel spécifique.</span><span class="sxs-lookup"><span data-stu-id="538c9-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="538c9-118">Cette fonction n’est actuellement pas utilisée par Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="538c9-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="538c9-119">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="538c9-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="538c9-120">Supprime toutes les données de sortie en file d’attente envoyées du serveur au client sur un canal virtuel spécifique.</span><span class="sxs-lookup"><span data-stu-id="538c9-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="538c9-121">Cette fonction n’est actuellement pas utilisée par Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="538c9-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="538c9-122">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="538c9-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="538c9-123">Retourne des informations sur un canal virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="538c9-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="538c9-124">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="538c9-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="538c9-125">Lit les données à partir de l’extrémité serveur d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="538c9-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="538c9-126">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="538c9-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="538c9-127">Écrit des données à l’extrémité serveur d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="538c9-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




