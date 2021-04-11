---
description: Capture vidéo sur un fichier Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Capture vidéo sur un fichier Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211244"
---
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="54ec7-103">Capture vidéo sur un fichier Windows Media</span><span class="sxs-lookup"><span data-stu-id="54ec7-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="54ec7-104">Pour capturer une vidéo et l’encoder dans un fichier Windows Media Video (WMV), connectez le code confidentiel de capture au filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) , comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="54ec7-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![graphique de capture Windows Media](images/vidcap03.png)

<span data-ttu-id="54ec7-106">Le moyen le plus simple de créer ce graphique est de spécifiez MEDIASUBTYPE \_ ASF dans la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="54ec7-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="54ec7-107">La valeur MEDIASUBTYPE \_ ASF indique au générateur de graphiques de capture d’utiliser le filtre de l’enregistreur ASF WM comme récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="54ec7-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="54ec7-108">Le générateur de graphiques de capture crée le filtre, l’ajoute au graphique et appelle [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) pour définir le nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="54ec7-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="54ec7-109">Elle retourne un pointeur vers le filtre en tant que paramètre sortant (</span><span class="sxs-lookup"><span data-stu-id="54ec7-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="54ec7-110">dans l’exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="54ec7-110">in the previous example).</span></span>

<span data-ttu-id="54ec7-111">Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) sur le writer WM ASF pour définir le profil Windows Media.</span><span class="sxs-lookup"><span data-stu-id="54ec7-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="54ec7-112">Vous devez effectuer cette opération avant de connecter des broches sur le writer WM ASF.</span><span class="sxs-lookup"><span data-stu-id="54ec7-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="54ec7-113">Pour plus d’informations sur la définition du profil, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="54ec7-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="54ec7-114">Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre de capture à l’enregistreur ASF :</span><span class="sxs-lookup"><span data-stu-id="54ec7-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="54ec7-115">Chaque broche d’entrée sur le filtre de l’enregistreur ASF WM correspond à un flux dans le profil Windows Media.</span><span class="sxs-lookup"><span data-stu-id="54ec7-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="54ec7-116">Vous devez connecter chaque code confidentiel afin que le contenu du fichier corresponde au profil.</span><span class="sxs-lookup"><span data-stu-id="54ec7-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54ec7-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54ec7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ec7-118">Capture vidéo dans un fichier</span><span class="sxs-lookup"><span data-stu-id="54ec7-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



