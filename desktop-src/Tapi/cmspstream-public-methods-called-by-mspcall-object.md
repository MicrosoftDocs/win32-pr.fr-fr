---
description: La liste suivante contient les méthodes CMSPStream appelées par l’objet MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Méthodes CMSPStream appelées par l’objet MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544286"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="a64dd-103">CMSPStream, méthodes publiques appelées par l’objet MSPCall</span><span class="sxs-lookup"><span data-stu-id="a64dd-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="a64dd-104">Méthodes publiques CMSPStream</span><span class="sxs-lookup"><span data-stu-id="a64dd-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="a64dd-105">Description</span><span class="sxs-lookup"><span data-stu-id="a64dd-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a64dd-106">**Rein**</span><span class="sxs-lookup"><span data-stu-id="a64dd-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="a64dd-107">Appelée par **MSPCall** lors de la création du flux.</span><span class="sxs-lookup"><span data-stu-id="a64dd-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="a64dd-108">**Correct**</span><span class="sxs-lookup"><span data-stu-id="a64dd-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="a64dd-109">Appelée par **MSPCall** pour désélectionner tous les objets terminal et libérer l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="a64dd-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="a64dd-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="a64dd-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="a64dd-111">Appelée par l’objet MSPCall pour recevoir l’état actuel du flux.</span><span class="sxs-lookup"><span data-stu-id="a64dd-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="a64dd-112">**HandleTSPData**</span><span class="sxs-lookup"><span data-stu-id="a64dd-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="a64dd-113">L’objet d’appel dérivé peut appeler cette méthode pour permettre au flux de gérer les commandes TSP.</span><span class="sxs-lookup"><span data-stu-id="a64dd-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="a64dd-114">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="a64dd-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="a64dd-115">Appelée par l’objet MSPCall pour permettre au flux de gérer les événements de graphique.</span><span class="sxs-lookup"><span data-stu-id="a64dd-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 



