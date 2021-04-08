---
description: Afficher les boîtes de dialogue de capture VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Afficher les boîtes de dialogue de capture VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745652"
---
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="37cd4-103">Afficher les boîtes de dialogue de capture VFW</span><span class="sxs-lookup"><span data-stu-id="37cd4-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="37cd4-104">Un périphérique de capture qui utilise encore un pilote de vidéo pour Windows (VFW) peut prendre en charge les trois boîtes de dialogue suivantes, qui sont utilisées pour configurer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="37cd4-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="37cd4-105">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="37cd4-105">Dialog box</span></span>    | <span data-ttu-id="37cd4-106">Description</span><span class="sxs-lookup"><span data-stu-id="37cd4-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cd4-107">Source vidéo</span><span class="sxs-lookup"><span data-stu-id="37cd4-107">Video Source</span></span>  | <span data-ttu-id="37cd4-108">Utilisé pour sélectionner l’entrée vidéo et ajuster les paramètres de l’appareil, tels que la luminosité ou le contraste de l’image.</span><span class="sxs-lookup"><span data-stu-id="37cd4-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="37cd4-109">Format vidéo</span><span class="sxs-lookup"><span data-stu-id="37cd4-109">Video Format</span></span>  | <span data-ttu-id="37cd4-110">Utilisé pour sélectionner les dimensions et la profondeur de l’image.</span><span class="sxs-lookup"><span data-stu-id="37cd4-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="37cd4-111">Affichage vidéo</span><span class="sxs-lookup"><span data-stu-id="37cd4-111">Video Display</span></span> | <span data-ttu-id="37cd4-112">Utilisé pour contrôler l’apparence de la vidéo rendue.</span><span class="sxs-lookup"><span data-stu-id="37cd4-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="37cd4-113">Pour afficher l’une de ces boîtes de dialogue, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="37cd4-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="37cd4-114">Arrêtez le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="37cd4-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="37cd4-115">Interrogez le filtre de capture de l’interface [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) .</span><span class="sxs-lookup"><span data-stu-id="37cd4-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="37cd4-116">Si **QueryInterface** se déroule correctement, cela signifie que l’appareil de capture est un appareil VFW.</span><span class="sxs-lookup"><span data-stu-id="37cd4-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="37cd4-117">Appelez [**IAMVfwCaptureDialogs :: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) pour vérifier si le pilote prend en charge la boîte de dialogue que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="37cd4-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="37cd4-118">L’énumération [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) définit des indicateurs pour chacune des boîtes de dialogue VFW.</span><span class="sxs-lookup"><span data-stu-id="37cd4-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="37cd4-119">**HasDialog** retourne S \_ OK si la boîte de dialogue est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37cd4-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="37cd4-120">\_Sinon, elle retourne la valeur false. par conséquent, vérifiez la valeur \_ OK directement, plutôt que d’utiliser la macro **Succeeded** .</span><span class="sxs-lookup"><span data-stu-id="37cd4-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="37cd4-121">Si la boîte de dialogue est prise en charge, appelez [**IAMVfwCaptureDialogs :: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="37cd4-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="37cd4-122">Redémarrez le graphique.</span><span class="sxs-lookup"><span data-stu-id="37cd4-122">Restart the graph.</span></span>

<span data-ttu-id="37cd4-123">Le code suivant illustre ces étapes pour la boîte de dialogue source vidéo :</span><span class="sxs-lookup"><span data-stu-id="37cd4-123">The following code shows these steps for the Video Source dialog box:</span></span>


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a><span data-ttu-id="37cd4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37cd4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37cd4-125">Configuration d’un périphérique de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="37cd4-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



