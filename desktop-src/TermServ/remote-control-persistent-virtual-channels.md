---
title: Canaux virtuels persistants de contrôle à distance
description: Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client. Les données continueront à être transmises et reçues via ce canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380327"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="f0b06-104">Canaux virtuels persistants de contrôle à distance</span><span class="sxs-lookup"><span data-stu-id="f0b06-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="f0b06-105">Sur Windows XP, une DLL peut spécifier un ou plusieurs canaux virtuels comme *contrôle à distance persistant*.</span><span class="sxs-lookup"><span data-stu-id="f0b06-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="f0b06-106">Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client.</span><span class="sxs-lookup"><span data-stu-id="f0b06-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="f0b06-107">Les données continueront à être transmises et reçues via ce canal.</span><span class="sxs-lookup"><span data-stu-id="f0b06-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="f0b06-108">Les canaux virtuels que la DLL ne spécifie pas en tant que contrôle à distance persistant se ferment dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="f0b06-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="f0b06-109">Les canaux virtuels persistants de contrôle à distance sont spécifiés lors de l’appel à **VirtualChannelInit**.</span><span class="sxs-lookup"><span data-stu-id="f0b06-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="f0b06-110">Pour plus d’informations à ce sujet, reportez-vous à la page de référence de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .</span><span class="sxs-lookup"><span data-stu-id="f0b06-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




