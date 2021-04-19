---
description: L’interface IDownloadJob définit les propriétés suivantes.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propriétés IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515267"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="40852-103">Propriétés IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="40852-103">IDownloadJob Properties</span></span>

<span data-ttu-id="40852-104">L’interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="40852-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="40852-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="40852-105">Property</span></span>                                        | <span data-ttu-id="40852-106">Description</span><span class="sxs-lookup"><span data-stu-id="40852-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40852-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="40852-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="40852-108">Obtient l’objet d’état spécifique à l’appelant qui est passé à la méthode [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .</span><span class="sxs-lookup"><span data-stu-id="40852-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="40852-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="40852-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="40852-110">Obtient le paramètre qui indique si l’appel à [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) a été traité complètement.</span><span class="sxs-lookup"><span data-stu-id="40852-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="40852-111">**Mises à jour**</span><span class="sxs-lookup"><span data-stu-id="40852-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="40852-112">Obtient une interface qui contient une collection en lecture seule des mises à jour spécifiées dans un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="40852-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



