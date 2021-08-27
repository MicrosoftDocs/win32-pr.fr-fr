---
description: Utilisation de l’énumérateur de périphérique système
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Utilisation de l’énumérateur de périphérique système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7192a1ea85d807dd388b79eef455edf59c83d3c22ab3a4a330799b3491253bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083532"
---
# <a name="using-the-system-device-enumerator"></a>Utilisation de l’énumérateur de périphérique système

L’énumérateur de périphérique système offre un moyen uniforme d’énumérer, par catégorie, les filtres inscrits sur le système d’un utilisateur. En outre, il fait la distinction entre les différents périphériques matériels, même si le même filtre les prend en charge. cela s’avère particulièrement utile pour les appareils qui utilisent le Windows Driver Model (WDM) et le filtre KSProxy. Par exemple, l’utilisateur peut avoir plusieurs périphériques de capture vidéo WDM, tous pris en charge par le même filtre. L’énumérateur de périphérique système les traite comme des instances d’appareil distinctes.

L’énumérateur de périphérique système fonctionne en créant un énumérateur pour une catégorie spécifique, telle que la capture audio ou la compression vidéo. L’énumérateur Category retourne un moniker unique pour chaque appareil de la catégorie. L’énumérateur de catégorie comprend automatiquement tous les appareils Plug-and-Play pertinents dans la catégorie. Pour obtenir la liste des catégories, consultez [Filtrer les catégories](filter-categories.md).

Pour utiliser l’énumérateur de périphérique système, procédez comme suit :

1.  Créez l’énumérateur de périphérique système en appelant **CoCreateInstance**. L’identificateur de classe (CLSID) est CLSID \_ SystemDeviceEnum.
2.  Obtenez un énumérateur de catégorie en appelant [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec le CLSID de la catégorie souhaitée. Cette méthode retourne un pointeur d’interface **IEnumMoniker** . Si la catégorie est vide (ou n’existe pas), la méthode retourne S \_ false au lieu d’un code d’erreur. Si c’est le cas, le pointeur **IEnumMoniker** retourné est **null** et son déréférencement entraîne une exception. Par conséquent, testez explicitement les \_ OK quand vous appelez **CreateClassEnumerator**, au lieu d’appeler la macro **Succeeded** habituelle.
3.  Utilisez la méthode **IEnumMoniker :: Next** pour énumérer chaque moniker. Cette méthode retourne un pointeur d’interface **IMoniker** . Lorsque la méthode **suivante** atteint la fin de l’énumération, elle retourne également la \_ valeur false. par conséquent, vérifiez de nouveau si la valeur est \_ OK.
4.  Pour récupérer le nom convivial de l’appareil (par exemple, pour l’afficher dans l’interface utilisateur), appelez la méthode **IMoniker :: BindToStorage** .
5.  pour créer et initialiser le filtre DirectShow qui gère l’appareil, appelez **IMoniker :: BindToObject** sur le moniker. Appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique.

Le diagramme suivant illustre ce processus.

![énumération des appareils](images/sysdevenum.png)

L’exemple suivant montre comment énumérer les compressions vidéo installées sur le système de l’utilisateur. Par souci de concision, l’exemple effectue une vérification des erreurs minimale.


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



**Monikers de périphérique**

Pour les monikers de périphérique, vous pouvez passer le moniker à la méthode [**IFilterGraph2 :: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) pour créer un filtre de capture pour l’appareil. Pour obtenir un exemple de code, consultez la documentation de cette méthode.

La méthode **IMoniker :: GetDisplayName** retourne le nom complet du moniker. Bien que le nom d’affichage soit lisible, vous ne l’affichez généralement pas pour un utilisateur final. À la place, récupérez le nom convivial à partir du conteneur des propriétés, comme décrit précédemment.

La méthode **IMoniker ::P arsedisplayname** ou la fonction **MkParseDisplayName** peut être utilisée pour créer un moniker de périphérique par défaut pour une catégorie de filtre donnée. Utilisez un nom complet au format `@device:*:{category-clsid}` , où `category-clsid` est la représentation sous forme de chaîne du GUID de la catégorie. Le moniker par défaut est le premier moniker retourné par l’énumérateur d’appareil pour cette catégorie.

 

 



