---
description: Cette rubrique explique comment énumérer les périphériques de capture vidéo sur le système des utilisateurs et comment créer une instance d’un appareil.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Énumération des périphériques de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393271"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="1ad9f-103">Énumération des périphériques de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="1ad9f-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="1ad9f-104">Cette rubrique explique comment énumérer les périphériques de capture vidéo sur le système de l’utilisateur et comment créer une instance d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="1ad9f-105">Pour énumérer les périphériques de capture vidéo sur le système, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1ad9f-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="1ad9f-106">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="1ad9f-107">Cette fonction reçoit un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1ad9f-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="1ad9f-108">Appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) pour définir l’attribut de type de source de l' [ \_ \_ attribut \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad9f-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="1ad9f-109">Définissez la valeur de l’attribut sur **MF \_ DEVSOURCE \_ attribut \_ source \_ type \_ VIDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="1ad9f-110">Appelez [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span><span class="sxs-lookup"><span data-stu-id="1ad9f-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="1ad9f-111">Cette fonction reçoit un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) et la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="1ad9f-112">Chaque pointeur représente un périphérique de capture vidéo distinct.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="1ad9f-113">Pour créer une instance d’un périphérique de capture :</span><span class="sxs-lookup"><span data-stu-id="1ad9f-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="1ad9f-114">Appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour obtenir un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="1ad9f-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="1ad9f-115">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="1ad9f-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="1ad9f-116">Après avoir créé la source du média, libérez les pointeurs d’interface et libérez de la mémoire pour le tableau :</span><span class="sxs-lookup"><span data-stu-id="1ad9f-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="1ad9f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ad9f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad9f-118">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="1ad9f-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



