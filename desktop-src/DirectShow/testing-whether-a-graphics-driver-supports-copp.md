---
description: Tester si un pilote graphique prend en charge COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Tester si un pilote graphique prend en charge COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651829"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Tester si un pilote graphique prend en charge COPP

Le protocole COPP (Certified Output Protection Protocol) permet à une application de protéger le contenu vidéo lorsqu’il transite de la carte vidéo au périphérique d’affichage. Si un pilote graphique prend en charge COPP, le pilote contient une chaîne de certificats signée par Microsoft, qui authentifie le pilote. Les applications de lecture qui utilisent COPP pour appliquer la protection du contenu doivent valider la chaîne de certificats pour s’assurer que le pilote n’a pas été falsifié.

Toutefois, vous souhaiterez peut-être vérifier si un pilote graphique prend en charge COPP, sans valider le certificat. Par exemple, lorsqu’un fournisseur de médias numériques émet une licence de gestion des droits numériques (DRM), il peut souhaiter vérifier si l’utilisateur dispose d’un pilote graphique compatible COPP. Le fournisseur n’a pas besoin d’appliquer COPP au moment où il émet la licence. il doit uniquement tester si le pilote prend en charge COPP.

Le code suivant montre comment tester si un pilote prend en charge COPP. L’application doit transmettre le nom d’un fichier vidéo qui sera utilisé pour tester le pilote. cela est nécessaire, car le filtre de convertisseur de mixage vidéo dans Microsoft® DirectShow® n’initialise pas une session COPP tant que le filtre n’est pas connecté. Cette fonction peut être incluse dans une application cliente pour vérifier si le pilote est capable d’exécuter COPP.

> [!Note]  
> Si l’ordinateur de l’utilisateur possède deux cartes graphiques, cette fonction teste le pilote de la carte graphique principale, mais pas la carte graphique secondaire.

 


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole de protection de sortie certifié](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



