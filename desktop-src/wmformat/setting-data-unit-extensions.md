---
title: Définition des extensions d’unité de données
description: Définition des extensions d’unité de données
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- extensions d’unité de données, définition
- flux, extensions d’unité de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104507831"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="f2600-107">Définition des extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="f2600-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="f2600-108">Certains flux sont configurés pour utiliser des extensions d’unité de données pour associer des données supplémentaires à des échantillons individuels.</span><span class="sxs-lookup"><span data-stu-id="f2600-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="f2600-109">Pour plus d’informations sur les exemples étendus, consultez [extensions d’unité de données](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="f2600-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="f2600-110">La plupart des systèmes d’extension d’unité de données requièrent une extension sur chaque échantillon dans le flux.</span><span class="sxs-lookup"><span data-stu-id="f2600-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="f2600-111">Si vous ne fournissez pas une extension de la taille correcte, l’enregistreur rejettera l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f2600-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="f2600-112">Pour ajouter des données étendues à un exemple, utilisez la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="f2600-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="f2600-113">Vous pouvez obtenir des informations sur les extensions d’unité de données configurées sur un flux à l’aide des méthodes [**IWMStreamConfig2 :: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) et [**IWMStreamConfig2 :: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="f2600-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2600-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2600-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2600-115">**Configuration d’extensions d’unité de données**</span><span class="sxs-lookup"><span data-stu-id="f2600-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="f2600-116">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="f2600-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




