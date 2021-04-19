---
description: Convertisseur de tee/récepteur à récepteur
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertisseur de tee/récepteur à récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541920"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="593a4-103">Convertisseur de tee/récepteur à récepteur</span><span class="sxs-lookup"><span data-stu-id="593a4-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="593a4-104">Le convertisseur tee/Sink-to-Sink est un filtre en mode noyau, KsProxy.</span><span class="sxs-lookup"><span data-stu-id="593a4-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="593a4-105">Il est utilisé dans les graphiques de filtres de télévision vidéo analogiques dans lesquels les données VBI sont rendues ou capturées.</span><span class="sxs-lookup"><span data-stu-id="593a4-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="593a4-106">Le filtre est connecté en amont au [filtre de capture vidéo WDM](wdm-video-capture-filter.md) et constitue un moyen efficace pour dupliquer des flux de données en mode noyau sans les transitions coûteuses entre le mode noyau et le mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="593a4-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="593a4-107">Il remet chaque bloc de données reçu à toutes les broches de sortie, et le codec en aval est chargé de rechercher les données VBI spécifiques à décoder.</span><span class="sxs-lookup"><span data-stu-id="593a4-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="593a4-108">Le convertisseur de tee/Sink-to-Sink apparaît dans la catégorie de filtre « périphériques de streaming WDM en t/Splitter » (AM \_ KSCATEGORY \_ Splitter).</span><span class="sxs-lookup"><span data-stu-id="593a4-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="593a4-109">Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="593a4-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="593a4-110">Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="593a4-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="593a4-111">Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="593a4-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="593a4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="593a4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="593a4-113">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="593a4-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
