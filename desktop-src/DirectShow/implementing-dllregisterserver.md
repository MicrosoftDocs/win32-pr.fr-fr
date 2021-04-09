---
description: Implémentation de DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implémentation de DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109526"
---
# <a name="implementing-dllregisterserver"></a>Implémentation de DllRegisterServer

La dernière étape consiste à implémenter la fonction **DllRegisterServer** . La DLL qui contient le composant doit exporter cette fonction. La fonction est appelée par une application de configuration, ou lorsque l’utilisateur exécute l’outil Regsvr32.exe.

L’exemple suivant montre une implémentation minimale de **DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



La fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crée des entrées de Registre pour chaque composant de la


```
g_Templates
```



. Toutefois, cette fonction présente des limitations. Tout d’abord, il affecte chaque filtre à la catégorie « filtres DirectShow » (CLSID \_ LegacyAmFilterCategory), mais tous les filtres n’appartiennent pas à cette catégorie. Les filtres de capture et les filtres de compression, par exemple, ont leurs propres catégories. Deuxièmement, si votre filtre prend en charge un périphérique matériel, vous devrez peut-être inscrire deux informations supplémentaires que **AMovieDLLRegisterServer2** ne gère pas : le *support* et la *catégorie pin*. Un support définit une méthode de communication dans un périphérique matériel, tel qu’un bus. La catégorie pin définit la fonction d’un code confidentiel. Pour plus d’informations sur les supports, consultez « KSPIN \_ Medium » dans le kit de développement de pilotes (DDK) Microsoft Windows. Pour obtenir la liste des catégories de code confidentiel, consultez [jeu de propriétés pin](pin-property-set.md).

Si vous souhaitez spécifier une catégorie de filtre, un support ou une catégorie de code confidentiel, appelez la méthode [**IFilterMapper2 :: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) à partir de **DllRegisterServer**. Cette méthode prend un pointeur vers une structure [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , qui spécifie des informations sur le filtre.

Pour compliquer un peu les choses, la structure **REGFILTER2** prend en charge deux formats différents pour l’inscription des codes confidentiels. Le membre **dwVersion** spécifie le format :

-   Si **dwVersion** est 1, le format pin est **AMOVIESETUP \_ pin** (décrit précédemment).
-   Si **dwVersion** est 2, le format de code confidentiel est [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).

La structure **REGFILTERPINS2** comprend des entrées pour les moyennes et les catégories de pin. En outre, il utilise des indicateurs binaires pour certains éléments que **AMOVIESETUP \_ pin** déclare comme valeurs booléennes.

L’exemple suivant montre comment appeler **IFilterMapper2 :: RegisterFilter** à l’intérieur de **DllRegisterServer**:


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



