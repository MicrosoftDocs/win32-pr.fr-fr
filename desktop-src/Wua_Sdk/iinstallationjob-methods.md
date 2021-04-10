---
description: L’interface IInstallationJob définit les méthodes suivantes.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Méthodes IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113535"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="fc4ad-103">Méthodes IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="fc4ad-103">IInstallationJob Methods</span></span>

<span data-ttu-id="fc4ad-104">L’interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) définit les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="fc4ad-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fc4ad-105">Method</span></span>                                                | <span data-ttu-id="fc4ad-106">Description</span><span class="sxs-lookup"><span data-stu-id="fc4ad-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc4ad-107">**Nettoyage**</span><span class="sxs-lookup"><span data-stu-id="fc4ad-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="fc4ad-108">Attend la fin d’une opération asynchrone, puis libère tous les rappels.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="fc4ad-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="fc4ad-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="fc4ad-110">Retourne une interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) qui décrit la progression actuelle d’une installation ou d’une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="fc4ad-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="fc4ad-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="fc4ad-112">Effectue une demande d’annulation de l’installation ou de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



