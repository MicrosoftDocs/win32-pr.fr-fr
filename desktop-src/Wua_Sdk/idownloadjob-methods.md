---
description: L’interface IDownloadJob définit les méthodes suivantes.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Méthodes IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526703"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="cdf2c-103">Méthodes IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="cdf2c-103">IDownloadJob Methods</span></span>

<span data-ttu-id="cdf2c-104">L’interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) définit les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="cdf2c-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="cdf2c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="cdf2c-105">Method</span></span>                                            | <span data-ttu-id="cdf2c-106">Description</span><span class="sxs-lookup"><span data-stu-id="cdf2c-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdf2c-107">**Nettoyage**</span><span class="sxs-lookup"><span data-stu-id="cdf2c-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="cdf2c-108">Attend la fin d’une opération asynchrone et libère tous les rappels.</span><span class="sxs-lookup"><span data-stu-id="cdf2c-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="cdf2c-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="cdf2c-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="cdf2c-110">Retourne une interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) qui décrit la progression actuelle d’un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="cdf2c-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="cdf2c-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="cdf2c-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="cdf2c-112">Effectue une demande pour mettre fin à un téléchargement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="cdf2c-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



