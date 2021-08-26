---
description: Sélection d’un périphérique de capture
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Sélection d’un périphérique de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bf92692070c8a0191a91559481d5446bf3d4d894c8e7f6aafc2ed9e73a6667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904409"
---
# <a name="selecting-a-capture-device"></a>Sélection d’un périphérique de capture

Pour sélectionner un périphérique de capture audio ou vidéo, utilisez l' [énumérateur de périphérique système](system-device-enumerator.md), décrit dans la rubrique [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md). L’énumérateur de périphérique système retourne une collection de monikers de périphérique, sélectionnée par catégorie d’appareil. Un *moniker* est un objet com qui contient des informations sur un autre objet. Les monikers permettent à l’application d’obtenir des informations sur un objet sans réellement créer l’objet. Plus tard, l’application peut utiliser le moniker pour créer l’objet. Pour plus d’informations sur les monikers, consultez la documentation de [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Pour utiliser l’énumérateur de périphérique système, procédez comme suit.

1.  Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’énumérateur du périphérique système.
2.  Appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) et spécifiez la catégorie d’appareil en tant que GUID. Pour les périphériques de capture, les catégories suivantes sont pertinentes. 

    | GUID de la catégorie                       | Description           |
    |-------------------------------------|-----------------------|
    | **CLSID \_ AudioInputDeviceCategory** | Périphériques de capture audio |
    | **CLSID \_ VideoInputDeviceCategory** | Périphériques de capture vidéo |

    

     

    Si une caméra vidéo a un microphone intégré, elle apparaît dans les deux catégories. Toutefois, la caméra et le microphone sont traités comme des appareils distincts par le système, à des fins d’énumération, de création d’appareils et de diffusion de données.

3.  La méthode [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) retourne un pointeur vers l’interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) . Pour énumérer les monikers, appelez [**IEnumMoniker :: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

Le code suivant crée un énumérateur pour une catégorie d’appareils spécifiée.


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



L’interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) énumère une liste d’interfaces [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , chacune représentant un moniker de périphérique. l’application peut lire les propriétés du moniker ou utiliser le moniker pour créer un filtre de capture DirectShow pour l’appareil. Les propriétés du moniker sont retournées en tant que valeurs de **type Variant** . Les propriétés suivantes sont prises en charge par les monikers de périphérique.



| Propriété       | Description                                                               | Type VARIANT |
|----------------|---------------------------------------------------------------------------|--------------|
| Convivial | Nom de l’appareil                                                   | **VT \_ BSTR** |
| Descriptive  | Description de l’appareil.                                              | **VT \_ BSTR** |
| DevicePath   | Chaîne unique qui identifie l’appareil. (Périphériques de capture vidéo uniquement.) | **VT \_ BSTR** |
| "WaveInID"     | Identificateur d’un périphérique de capture audio. (Périphériques de capture audio uniquement.) | **VT \_**   |



 

Les propriétés « FriendlyName » et « description » conviennent à l’affichage dans une interface utilisateur.

-   La propriété « FriendlyName » est disponible pour chaque appareil. Il contient un nom explicite pour l’appareil.
-   La propriété « Description » est disponible uniquement pour les appareils caméscopes DV et D-VHS/MPEG. Pour plus d’informations, consultez [pilote MSDV](msdv-driver.md) et [pilote MSTape](mstape-driver.md). S’il est disponible, il contient une description de l’appareil qui est plus spécifique que la propriété « FriendlyName ». En général, il comprend le nom du fournisseur.
-   La propriété « DevicePath » n’est pas une chaîne explicite, mais elle est toujours unique pour chaque périphérique de capture vidéo sur le système. Vous pouvez utiliser cette propriété pour faire la distinction entre deux ou plusieurs instances du même modèle de périphérique.
-   si la propriété « WaveInID » est présente, cela signifie que le filtre de capture DirectShow utilise les api [Audio Waveform](../multimedia/waveform-audio.md) en interne pour communiquer avec l’appareil. La valeur de la propriété « WaveInID » correspond à l’identificateur utilisé par les fonctions «*Wave \**», telles que [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Pour lire les propriétés du moniker, procédez comme suit.

1.  Appelez [**IMoniker :: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) pour obtenir un pointeur vers l’interface [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .
2.  Appelez **IPropertyBag :: Read** pour lire la propriété.

L’exemple de code suivant montre comment énumérer une liste de monikers de périphériques et obtenir les propriétés.


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



pour créer un filtre de capture DirectShow pour l’appareil, appelez la méthode [**IMoniker :: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) pour obtenir un pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Appelez ensuite [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique de filtre :


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture audio](audio-capture.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 
