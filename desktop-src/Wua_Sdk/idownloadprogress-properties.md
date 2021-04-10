---
description: L’interface IDownloadProgress définit les propriétés suivantes.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propriétés IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951236"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="fdf59-103">Propriétés IDownloadProgress</span><span class="sxs-lookup"><span data-stu-id="fdf59-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="fdf59-104">L’interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fdf59-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="fdf59-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="fdf59-105">Property</span></span>                                                                               | <span data-ttu-id="fdf59-106">Description</span><span class="sxs-lookup"><span data-stu-id="fdf59-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdf59-107">**CurrentUpdateBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="fdf59-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="fdf59-108">Obtient une chaîne qui spécifie la quantité de données transférées pour le ou les fichiers de la mise à jour en cours de téléchargement, en octets.</span><span class="sxs-lookup"><span data-stu-id="fdf59-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="fdf59-109">**CurrentUpdateBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="fdf59-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="fdf59-110">Obtient une chaîne qui estime la quantité de données à transférer pour le ou les fichiers de la mise à jour en cours de téléchargement, en octets.</span><span class="sxs-lookup"><span data-stu-id="fdf59-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="fdf59-111">**CurrentUpdateDownloadPhase**</span><span class="sxs-lookup"><span data-stu-id="fdf59-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="fdf59-112">Obtient une valeur d’énumération [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) qui spécifie la phase du téléchargement actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="fdf59-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="fdf59-113">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="fdf59-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="fdf59-114">Obtient une valeur d’index de base zéro qui spécifie la mise à jour en cours de téléchargement lorsque plusieurs mises à jour ont été sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="fdf59-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="fdf59-115">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="fdf59-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="fdf59-116">Obtient une estimation du pourcentage de la mise à jour actuelle qui a été téléchargée.</span><span class="sxs-lookup"><span data-stu-id="fdf59-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="fdf59-117">**PourcentageAchevé**</span><span class="sxs-lookup"><span data-stu-id="fdf59-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="fdf59-118">Obtient une estimation du pourcentage de toutes les mises à jour qui ont été téléchargées.</span><span class="sxs-lookup"><span data-stu-id="fdf59-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="fdf59-119">**TotalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="fdf59-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="fdf59-120">Obtient une chaîne qui spécifie la quantité totale de données téléchargées, en octets.</span><span class="sxs-lookup"><span data-stu-id="fdf59-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="fdf59-121">**TotalBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="fdf59-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="fdf59-122">Obtient une chaîne qui représente l’estimation de la quantité totale de données qui seront téléchargées, en octets.</span><span class="sxs-lookup"><span data-stu-id="fdf59-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



