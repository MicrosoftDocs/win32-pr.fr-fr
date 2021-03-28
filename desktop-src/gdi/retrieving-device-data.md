---
description: 'Les applications peuvent utiliser les fonctions suivantes pour récupérer des données d’appareil à l’aide d’un contexte de périphérique : GetDeviceCaps et DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Récupération des données de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972526"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="adbcc-103">Récupération des données de l’appareil</span><span class="sxs-lookup"><span data-stu-id="adbcc-103">Retrieving Device Data</span></span>

<span data-ttu-id="adbcc-104">Les applications peuvent utiliser les fonctions suivantes pour récupérer des données d’appareil à l’aide d’un contexte de périphérique : [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) et [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span><span class="sxs-lookup"><span data-stu-id="adbcc-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="adbcc-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) récupère les données générales des appareils suivants :</span><span class="sxs-lookup"><span data-stu-id="adbcc-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="adbcc-106">Affichages raster</span><span class="sxs-lookup"><span data-stu-id="adbcc-106">Raster displays</span></span>
-   <span data-ttu-id="adbcc-107">Imprimantes matricielles</span><span class="sxs-lookup"><span data-stu-id="adbcc-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="adbcc-108">Imprimantes jet d’encre</span><span class="sxs-lookup"><span data-stu-id="adbcc-108">Ink-jet printers</span></span>
-   <span data-ttu-id="adbcc-109">Imprimantes laser</span><span class="sxs-lookup"><span data-stu-id="adbcc-109">Laser printers</span></span>
-   <span data-ttu-id="adbcc-110">Traceurs vectoriels</span><span class="sxs-lookup"><span data-stu-id="adbcc-110">Vector plotters</span></span>
-   <span data-ttu-id="adbcc-111">Caméras raster</span><span class="sxs-lookup"><span data-stu-id="adbcc-111">Raster cameras</span></span>

<span data-ttu-id="adbcc-112">Les données incluent les fonctionnalités prises en charge de l’appareil, y compris la résolution de l’appareil (pour les affichages vidéo), le format de couleur (pour les affichages vidéo et les imprimantes couleur), le nombre d’objets graphiques, les fonctionnalités raster, le dessin courbé, le dessin en courbes, le dessin polygonal et le dessin de texte.</span><span class="sxs-lookup"><span data-stu-id="adbcc-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="adbcc-113">Une application récupère ces données en fournissant un handle identifiant le contexte de périphérique approprié, ainsi qu’un index spécifiant le type de données que la fonction doit récupérer.</span><span class="sxs-lookup"><span data-stu-id="adbcc-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="adbcc-114">La fonction [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) récupère les données spécifiques aux imprimantes, y compris le nombre d’emplacements de papier disponibles, les fonctionnalités duplex de l’imprimante, les résolutions prises en charge par l’imprimante, le format de papier maximal et minimal pris en charge, etc.</span><span class="sxs-lookup"><span data-stu-id="adbcc-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="adbcc-115">Une application récupère ces données en fournissant des chaînes qui spécifient un périphérique et un port d’imprimante, ainsi qu’un index spécifiant le type de données que la fonction doit récupérer.</span><span class="sxs-lookup"><span data-stu-id="adbcc-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
