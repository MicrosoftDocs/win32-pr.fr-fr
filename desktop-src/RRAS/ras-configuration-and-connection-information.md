---
title: Configuration RAS et informations de connexion
description: Les applications qui s’exécutent sur Windows NT 4,0 et versions ultérieures, ainsi que sur Windows 95, peuvent utiliser la fonction RasEnumConnections pour obtenir des informations sur les connexions existantes sur l’ordinateur local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuration et connexion, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511424"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="3ff6a-104">Configuration RAS et informations de connexion</span><span class="sxs-lookup"><span data-stu-id="3ff6a-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="3ff6a-105">Les applications qui s’exécutent sur Windows NT 4,0 et versions ultérieures, ainsi que sur Windows 95, peuvent utiliser la fonction [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) pour obtenir des informations sur les connexions existantes sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="3ff6a-106">Les informations relatives à chaque connexion incluent un descripteur de connexion et le nom de l’entrée de l’annuaire téléphonique utilisée pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="3ff6a-107">Vous pouvez utiliser le descripteur de connexion dans un appel à la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour obtenir l’état actuel de la connexion.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="3ff6a-108">Windows NT Server 4,0 et versions ultérieures fournissent deux nouvelles fonctions pour récupérer les informations RAS.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="3ff6a-109">Windows 95does ne prend pas en charge ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="3ff6a-110">La fonction [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) retourne le nom et le type des appareils prenant en charge RAS qui sont configurés sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="3ff6a-111">La fonction [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) spécifie un objet d’événement que le système signale lorsqu’une connexion RAS est créée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




