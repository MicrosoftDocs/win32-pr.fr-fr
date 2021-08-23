---
description: Définition des propriétés de compression vidéo
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Définition des propriétés de compression vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583279"
---
# <a name="setting-video-compression-properties"></a>Définition des propriétés de compression vidéo

Les filtres de compression vidéo peuvent prendre en charge l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) sur leurs broches de sortie. Utilisez cette interface pour définir les propriétés de compression, telles que la fréquence d’images clés, le nombre d’images prédites (P) par image clé et la qualité de compression relative.

Tout d’abord, appelez la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) pour rechercher la broche de sortie du filtre, puis interrogez le code confidentiel de l’interface. Certains filtres peuvent ne pas prendre en charge l’interface du tout. D’autres peuvent exposer l’interface, mais ne prennent pas en charge chaque propriété de compression. Pour déterminer les propriétés prises en charge, appelez [**IAMVideoCompression :: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Cette méthode retourne plusieurs éléments d’information :

-   Un ensemble d’indicateurs de fonctionnalités
-   Chaîne descriptive et chaîne de numéro de version
-   Valeurs par défaut pour la fréquence d’images clés, la fréquence d’images P et la qualité (en cas de prise en charge)

La méthode a la syntaxe suivante :


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



Les paramètres *pszVersion* et *pszDesc* sont des mémoires tampons à caractères larges qui reçoivent la chaîne de version et la chaîne de description. Les paramètres *cbVersion* et *cbDesc* reçoivent les tailles de mémoire tampon requises en octets (et non en caractères). Les paramètres *lKeyFrame*, *lPFrame* et *dblQuality* reçoivent les valeurs par défaut pour la fréquence d’images clé, la fréquence d’images P et la qualité. La qualité est exprimée sous la forme d’un nombre à virgule flottante compris entre 0,0 et 1,0. Le paramètre *lCap* reçoit **une opération or au niveau du bit** des indicateurs de fonctionnalités, qui sont définis par le type énuméré [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .

L’un de ces paramètres peut être **null**, auquel cas la méthode ignore ce paramètre. Par exemple, pour allouer des tampons pour les chaînes de version et de description, appelez d’abord la méthode avec **null** dans les premier et troisième paramètres. Utilisez les valeurs retournées pour *cbVersion* et *cbDesc* pour allouer les mémoires tampons, puis appelez à nouveau la méthode :


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



La valeur de *lCap* indique laquelle des autres méthodes **IAMVideoCompression** prend en charge le filtre. Par exemple, si *lCap* contient l' \_ indicateur CompressionCaps CanKeyFrame, vous pouvez appeler [**IAMVideoCompression :: obtenir \_ keycadence**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) pour obtenir la fréquence d’images clé et [**IAMVideoCompression ::p ut \_**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) pour définir la fréquence d’images clé. Une valeur négative indique que le filtre utilisera la valeur par défaut, telle qu’elle est obtenue à partir de [**IAMVideoCompression :: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Par exemple :


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



L’exemple de code suivant tente de trouver l’interface **IAMVideoCompression** sur la broche de sortie. Si elle est réussie, elle récupère les valeurs par défaut et réelles des propriétés de compression :


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> Si vous utilisez l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) pour générer votre graphique, vous pouvez obtenir l’interface **IAMVideoCompression** en appelant [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), au lieu d’utiliser **IBaseFilter :: EnumPins**. La méthode **FindInterface** est une méthode d’assistance qui recherche des filtres et des codes confidentiels dans le graphique pour une interface spécifiée.

 

 

 



