---
title: Prise en charge des codes temporels SMPTE
description: Prise en charge des codes temporels SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK, codes temporels SMPTE
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- Windows Media Format SDK, interface IWMReaderTimecode
- ASF (Advanced Systems Format), interface IWMReaderTimecode
- ASF (format des systèmes avancés), interface IWMReaderTimecode
- Codes temporels SMPTE, à propos de
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507795"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="df437-111">Prise en charge des codes temporels SMPTE</span><span class="sxs-lookup"><span data-stu-id="df437-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="df437-112">Le kit de développement logiciel (SDK) du format Windows Media offre une prise en charge limitée du code temporel SMPTE, qui est un format de code de temps standard pour les films et la télévision.</span><span class="sxs-lookup"><span data-stu-id="df437-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="df437-113">Vous pouvez inclure des données de code temporel SMPTE avec des exemples comme extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="df437-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="df437-114">La partie données de l’extension est une structure de [**\_ données d' \_ extension \_ de code**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) d’exécution WMT qui contient les informations de l’horodatage SMPTE d’origine.</span><span class="sxs-lookup"><span data-stu-id="df437-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="df437-115">La conservation du code temporel SMPTE dans vos fichiers ASF est accompagnée de limites de performances.</span><span class="sxs-lookup"><span data-stu-id="df437-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="df437-116">Chaque échantillon avec un horodatage SMPTE associé nécessite le transport des 14 octets dans la structure de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="df437-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="df437-117">Dans un scénario de diffusion en continu, cette exigence accrue en bande passante peut être catastrophique.</span><span class="sxs-lookup"><span data-stu-id="df437-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="df437-118">Par conséquent, il est recommandé de conserver les codes temporels SMPTE uniquement dans les fichiers ASF pendant le processus de modification vidéo, ce qui est généralement fait avec des fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="df437-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="df437-119">Une fois le fichier final créé, vous devez supprimer les extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="df437-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="df437-120">Vous pouvez lire les horodatages SMPTE comme vous le feriez pour n’importe quelle autre extension d’unité de données, mais les objets de lecture offrent une prise en charge intégrée de la recherche par code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="df437-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="df437-121">Pour pouvoir Rechercher les horodatages SMPTE, vous devez d’abord indexer le fichier par code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="df437-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="df437-122">Vous pouvez configurer l’indexeur de façon à indexer les codes de temps à l’aide de la méthode [**IWMIndexer2 :: configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .</span><span class="sxs-lookup"><span data-stu-id="df437-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="df437-123">À l’aide du lecteur asynchrone, vous pouvez naviguer dans un fichier à l’aide des horodatages SMPTE à l’aide des méthodes de l’interface [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) et de la méthode [**IWMReaderAdvanced3 :: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) .</span><span class="sxs-lookup"><span data-stu-id="df437-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="df437-124">Avec le lecteur synchrone, utilisez [**IWMSyncReader2 :: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span><span class="sxs-lookup"><span data-stu-id="df437-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df437-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df437-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df437-126">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="df437-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="df437-127">**Configuration d’extensions d’unité de données**</span><span class="sxs-lookup"><span data-stu-id="df437-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




