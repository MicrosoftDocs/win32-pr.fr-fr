---
title: Configuration des flux de transfert de fichiers
description: Configuration des flux de transfert de fichiers
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flux, configuration des flux de transfert de fichiers
- codecs, configuration des flux de transfert de fichiers
- flux de transfert de fichiers
- flux, extensions d’unité de données
- codecs, extensions d’unité de données
- extensions d’unité de données, flux de transfert de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030841"
---
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="73f38-109">Configuration des flux de transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="73f38-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="73f38-110">Les flux de transfert de fichiers ne nécessitent pas de paramètres spéciaux dans la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="73f38-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="73f38-111">Ils requièrent une extension d’unité de données pour associer un nom de fichier à chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="73f38-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="73f38-112">Pour envoyer un nom avec des exemples de transfert de fichiers, vous devez implémenter un système d’extension d’unité de données pour le flux.</span><span class="sxs-lookup"><span data-stu-id="73f38-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="73f38-113">Pour définir une extension d’unité de données pour le flux, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="73f38-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="73f38-114">Obtenez un pointeur vers l’interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="73f38-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="73f38-115">Ajoutez une extension d’unité de données pour le flux en appelant [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) comme suit :</span><span class="sxs-lookup"><span data-stu-id="73f38-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="73f38-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73f38-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f38-117">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="73f38-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="73f38-118">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="73f38-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="73f38-119">**Flux de fichiers**</span><span class="sxs-lookup"><span data-stu-id="73f38-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




