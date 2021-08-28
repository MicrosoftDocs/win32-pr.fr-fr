---
description: Énumération des effets et des transitions
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Énumération des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd94dee9ff6774e9608d6b599986c0b943b60d335df2ab9b27e8c2eb64d7fe42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685809"
---
# <a name="enumerating-effects-and-transitions"></a>Énumération des effets et des transitions

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

DirectShow fournit un objet [énumérateur de périphérique système](system-device-enumerator.md) pour l’énumération des appareils. Vous pouvez l’utiliser pour récupérer les monikers des effets ou des transitions installés sur le système de l’utilisateur.

L’énumérateur de périphérique système expose l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) . Elle retourne les énumérateurs de catégorie pour les catégories d’appareils spécifiées. Un énumérateur de catégorie, à son tour, expose l’interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) et retourne des monikers pour chaque appareil de la catégorie. Pour une présentation détaillée de l’utilisation de **ICreateDevEnum**, consultez [énumération d’appareils et de filtres](enumerating-devices-and-filters.md). voici un bref résumé, propre à DirectShow Services d’édition.

Pour énumérer des effets ou des transitions, procédez comme suit.

1.  Créez une instance de l’énumérateur du périphérique système.
2.  Appelez la méthode [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) pour récupérer un énumérateur de catégorie. Les catégories sont définies par des identificateurs de classe (CLSID). Utilisez CLSID \_ VideoEffects1Category pour les effets ou les \_ VideoEffects2Category CLSID pour les transitions.
3.  Appelez **IEnumMoniker :: Next** pour récupérer chaque moniker dans l’énumération.
4.  Pour chaque moniker, appelez **IMoniker :: BindToStorage** pour récupérer son conteneur de propriétés associé.

Le conteneur de propriétés contient le nom convivial et l’identificateur global unique (GUID) de l’effet ou de la transition. Une application peut afficher une liste de noms conviviaux, puis obtenir le GUID correspondant.

L’exemple de code suivant illustre ces étapes.


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
