---
description: Tester si un pilote graphique prend en charge COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Tester si un pilote graphique prend en charge COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544300"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a><span data-ttu-id="59ee9-103">Tester si un pilote graphique prend en charge COPP</span><span class="sxs-lookup"><span data-stu-id="59ee9-103">Testing Whether a Graphics Driver Supports COPP</span></span>

<span data-ttu-id="59ee9-104">Le protocole COPP (Certified Output Protection Protocol) permet à une application de protéger le contenu vidéo lorsqu’il transite de la carte vidéo au périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="59ee9-104">Certified Output Protection Protocol (COPP) enables an application to protect video content as it travels from the video card to the display device.</span></span> <span data-ttu-id="59ee9-105">Si un pilote graphique prend en charge COPP, le pilote contient une chaîne de certificats signée par Microsoft, qui authentifie le pilote.</span><span class="sxs-lookup"><span data-stu-id="59ee9-105">If a graphics driver supports COPP, the driver holds a certificate chain, signed by Microsoft, authenticating the driver.</span></span> <span data-ttu-id="59ee9-106">Les applications de lecture qui utilisent COPP pour appliquer la protection du contenu doivent valider la chaîne de certificats pour s’assurer que le pilote n’a pas été falsifié.</span><span class="sxs-lookup"><span data-stu-id="59ee9-106">Playback applications that use COPP to enforce content protection must validate the certificate chain to ensure that the driver has not been tampered with.</span></span>

<span data-ttu-id="59ee9-107">Toutefois, vous souhaiterez peut-être vérifier si un pilote graphique prend en charge COPP, sans valider le certificat.</span><span class="sxs-lookup"><span data-stu-id="59ee9-107">However, you might want to check whether a graphics driver supports COPP, without validating the certificate.</span></span> <span data-ttu-id="59ee9-108">Par exemple, lorsqu’un fournisseur de médias numériques émet une licence de gestion des droits numériques (DRM), il peut souhaiter vérifier si l’utilisateur dispose d’un pilote graphique compatible COPP.</span><span class="sxs-lookup"><span data-stu-id="59ee9-108">For example, when a digital media provider issues a digital rights management (DRM) license, it might want to check whether the user has a COPP-enabled graphics driver.</span></span> <span data-ttu-id="59ee9-109">Le fournisseur n’a pas besoin d’appliquer COPP au moment où il émet la licence. il doit uniquement tester si le pilote prend en charge COPP.</span><span class="sxs-lookup"><span data-stu-id="59ee9-109">The provider does not need to enforce COPP at the time it issues the license; it only needs to test whether the driver supports COPP.</span></span>

<span data-ttu-id="59ee9-110">Le code suivant montre comment tester si un pilote prend en charge COPP.</span><span class="sxs-lookup"><span data-stu-id="59ee9-110">The following code shows how to test whether a driver supports COPP.</span></span> <span data-ttu-id="59ee9-111">L’application doit transmettre le nom d’un fichier vidéo qui sera utilisé pour tester le pilote.</span><span class="sxs-lookup"><span data-stu-id="59ee9-111">The application must pass in the name of a video file that will be used to test the driver.</span></span> <span data-ttu-id="59ee9-112">Cela est nécessaire, car le filtre de convertisseur de mixage vidéo dans Microsoft® DirectShow® n’initialise pas une session COPP tant que le filtre n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="59ee9-112">This is required because the Video Mixing Renderer filter in Microsoft® DirectShow® does not initialize a COPP session until the filter is connected.</span></span> <span data-ttu-id="59ee9-113">Cette fonction peut être incluse dans une application cliente pour vérifier si le pilote est capable d’exécuter COPP.</span><span class="sxs-lookup"><span data-stu-id="59ee9-113">This function can be included in a client application to check if the driver is capable of running COPP.</span></span>

> [!Note]  
> <span data-ttu-id="59ee9-114">Si l’ordinateur de l’utilisateur possède deux cartes graphiques, cette fonction teste le pilote de la carte graphique principale, mais pas la carte graphique secondaire.</span><span class="sxs-lookup"><span data-stu-id="59ee9-114">If the user's computer has two graphics cards, this function tests the driver for the primary graphics card, but not the secondary graphics card.</span></span>

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a><span data-ttu-id="59ee9-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59ee9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59ee9-116">Utilisation du protocole de protection de sortie certifié</span><span class="sxs-lookup"><span data-stu-id="59ee9-116">Using Certified Output Protection Protocol</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



