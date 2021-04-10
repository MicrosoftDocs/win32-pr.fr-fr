---
title: Pour connaître les statistiques de l’enregistreur
description: Pour connaître les statistiques de l’enregistreur
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- ASF (Advanced Systems Format), statistiques de l’enregistreur
- ASF (format des systèmes avancés), statistiques de l’enregistreur
- statistiques de l’enregistreur, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103940760"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="77e98-106">Pour connaître les statistiques de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="77e98-106">To Get Writer Statistics</span></span>

<span data-ttu-id="77e98-107">Le writer peut fournir des informations statistiques sur l’écriture d’opérations.</span><span class="sxs-lookup"><span data-stu-id="77e98-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="77e98-108">Il existe deux méthodes pour collecter des statistiques d’enregistreur : [**IWMWriterAdvanced :: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) et [**IWMWriterAdvanced3 :: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span><span class="sxs-lookup"><span data-stu-id="77e98-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="77e98-109">Les informations extraites par **GetStatisticsEx** sont plus spécifiques que les informations récupérées par **GetStatistics**.</span><span class="sxs-lookup"><span data-stu-id="77e98-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="77e98-110">Les deux méthodes remplissent des structures avec des informations statistiques.</span><span class="sxs-lookup"><span data-stu-id="77e98-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="77e98-111">**GetStatistics** utilise la structure de statistiques de l' [**\_ \_ enregistreur WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) et **GetStatisticsEx** utilise la structure des statistiques de l' [**\_ enregistreur WM \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) .</span><span class="sxs-lookup"><span data-stu-id="77e98-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="77e98-112">**GetStatisticsEx** ne duplique pas les données obtenues par **GetStatistics**.</span><span class="sxs-lookup"><span data-stu-id="77e98-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="77e98-113">Pour obtenir les informations les plus complètes, vous devez appeler les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="77e98-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77e98-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77e98-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e98-115">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="77e98-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="77e98-116">**Interface IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="77e98-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="77e98-117">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="77e98-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




