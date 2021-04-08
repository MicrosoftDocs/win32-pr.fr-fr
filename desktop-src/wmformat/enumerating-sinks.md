---
title: Énumération des récepteurs
description: Énumération des récepteurs
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- ASF (Advanced Systems Format), énumération des récepteurs
- ASF (format avancé des systèmes), énumération des récepteurs
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724031"
---
# <a name="enumerating-sinks"></a><span data-ttu-id="67c85-108">Énumération des récepteurs</span><span class="sxs-lookup"><span data-stu-id="67c85-108">Enumerating Sinks</span></span>

<span data-ttu-id="67c85-109">Plusieurs récepteurs peuvent être associés à l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="67c85-109">The writer can have many sinks associated with it.</span></span> <span data-ttu-id="67c85-110">Vous pouvez énumérer les récepteurs qui ont été ajoutés au writer à l’aide de [**IWMWriterAdvanced :: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) et [**IWMWriterAdvanced :: GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span><span class="sxs-lookup"><span data-stu-id="67c85-110">You can enumerate the sinks that have been added to the writer by using [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) and [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span></span>

<span data-ttu-id="67c85-111">L’exemple de code dans l' [obtention de messages d’erreur à partir d’un récepteur](getting-error-messages-from-a-sink.md) démontre l’énumération du récepteur.</span><span class="sxs-lookup"><span data-stu-id="67c85-111">The example code in the [Getting Error Messages from a Sink](getting-error-messages-from-a-sink.md) demonstrates sink enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="67c85-112">Lors de l’énumération des récepteurs, le récepteur de fichiers par défaut créé en réponse à un appel à [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) est énuméré avec tout autre récepteur que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="67c85-112">When enumerating sinks, the default file sink created in response to a call to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) will be enumerated along with any other sinks you have added.</span></span> <span data-ttu-id="67c85-113">Si vous utilisez uniquement le récepteur de fichiers par défaut, vous pouvez y accéder en appelant **GetSink** pour l’index de récepteur 0.</span><span class="sxs-lookup"><span data-stu-id="67c85-113">If you are using only the default file sink, you can access it by calling **GetSink** for sink index 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="67c85-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67c85-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67c85-115">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="67c85-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="67c85-116">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="67c85-116">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




