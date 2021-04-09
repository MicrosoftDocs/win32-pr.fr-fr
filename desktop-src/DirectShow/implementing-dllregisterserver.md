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
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="1dfd3-103">Implémentation de DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="1dfd3-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="1dfd3-104">La dernière étape consiste à implémenter la fonction **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="1dfd3-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="1dfd3-105">La DLL qui contient le composant doit exporter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="1dfd3-106">La fonction est appelée par une application de configuration, ou lorsque l’utilisateur exécute l’outil Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="1dfd3-107">L’exemple suivant montre une implémentation minimale de **DlLRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="1dfd3-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="1dfd3-108">La fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crée des entrées de Registre pour chaque composant de la</span><span class="sxs-lookup"><span data-stu-id="1dfd3-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="1dfd3-109">.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-109">array.</span></span> <span data-ttu-id="1dfd3-110">Toutefois, cette fonction présente des limitations.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-110">However, this function has some limitations.</span></span> <span data-ttu-id="1dfd3-111">Tout d’abord, il affecte chaque filtre à la catégorie « filtres DirectShow » (CLSID \_ LegacyAmFilterCategory), mais tous les filtres n’appartiennent pas à cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="1dfd3-112">Les filtres de capture et les filtres de compression, par exemple, ont leurs propres catégories.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="1dfd3-113">Deuxièmement, si votre filtre prend en charge un périphérique matériel, vous devrez peut-être inscrire deux informations supplémentaires que **AMovieDLLRegisterServer2** ne gère pas : le *support* et la *catégorie pin*.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="1dfd3-114">Un support définit une méthode de communication dans un périphérique matériel, tel qu’un bus.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="1dfd3-115">La catégorie pin définit la fonction d’un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="1dfd3-116">Pour plus d’informations sur les supports, consultez « KSPIN \_ Medium » dans le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="1dfd3-117">Pour obtenir la liste des catégories de code confidentiel, consultez [jeu de propriétés pin](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="1dfd3-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="1dfd3-118">Si vous souhaitez spécifier une catégorie de filtre, un support ou une catégorie de code confidentiel, appelez la méthode [**IFilterMapper2 :: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) à partir de **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="1dfd3-119">Cette méthode prend un pointeur vers une structure [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , qui spécifie des informations sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="1dfd3-120">Pour compliquer un peu les choses, la structure **REGFILTER2** prend en charge deux formats différents pour l’inscription des codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="1dfd3-121">Le membre **dwVersion** spécifie le format :</span><span class="sxs-lookup"><span data-stu-id="1dfd3-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="1dfd3-122">Si **dwVersion** est 1, le format pin est **AMOVIESETUP \_ pin** (décrit précédemment).</span><span class="sxs-lookup"><span data-stu-id="1dfd3-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="1dfd3-123">Si **dwVersion** est 2, le format de code confidentiel est [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span><span class="sxs-lookup"><span data-stu-id="1dfd3-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="1dfd3-124">La structure **REGFILTERPINS2** comprend des entrées pour les moyennes et les catégories de pin.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="1dfd3-125">En outre, il utilise des indicateurs binaires pour certains éléments que **AMOVIESETUP \_ pin** déclare comme valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="1dfd3-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="1dfd3-126">L’exemple suivant montre comment appeler **IFilterMapper2 :: RegisterFilter** à l’intérieur de **DllRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="1dfd3-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


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



 

 



