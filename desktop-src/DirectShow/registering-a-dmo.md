---
description: Inscription d’un DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Inscription d’un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515895"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="ab573-103">Inscription d’un DMO</span><span class="sxs-lookup"><span data-stu-id="ab573-103">Registering a DMO</span></span>

<span data-ttu-id="ab573-104">Pour que les clients utilisent votre DMO, le CLSID doit être inscrit sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab573-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="ab573-105">Cette opération s’effectue par le biais de la fonction **DllRegisterServer** de la dll.</span><span class="sxs-lookup"><span data-stu-id="ab573-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="ab573-106">Si vous utilisez la Active Template Library (ATL), l’Assistant ATL génère automatiquement cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ab573-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="ab573-107">Vous pouvez également inscrire votre DMO sous une ou plusieurs catégories DMO standard.</span><span class="sxs-lookup"><span data-stu-id="ab573-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="ab573-108">Cela permet aux clients de découvrir votre DMO à l’aide de la fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="ab573-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="ab573-109">Les catégories sont définies par le GUID et sont répertoriées dans la section [GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ab573-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="ab573-110">L’inscription d’un module DMO dans une catégorie est facultative.</span><span class="sxs-lookup"><span data-stu-id="ab573-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="ab573-111">Pour ce faire, appelez la fonction [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) et spécifiez le nom convivial de DMO, le CLSID et la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ab573-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="ab573-112">Si vous le souhaitez, vous pouvez également inscrire un ensemble de types de médias pris en charge par votre DMOs.</span><span class="sxs-lookup"><span data-stu-id="ab573-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="ab573-113">Pour plus d’informations, consultez [types de média DMO](dmo-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="ab573-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="ab573-114">L’exemple suivant montre comment enregistrer un effet audio DMO qui prend en charge l’entrée et la sortie audio PCM.</span><span class="sxs-lookup"><span data-stu-id="ab573-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="ab573-115">Dans ce cas, les types d’entrée et de sortie sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="ab573-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="ab573-116">Cet exemple suppose que ATL a été utilisé pour créer le projet. la dernière ligne de la fonction appelle la méthode ATL standard pour inscrire le serveur COM.</span><span class="sxs-lookup"><span data-stu-id="ab573-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="ab573-117">Si vous n’utilisez pas ATL, votre fonction sera différente.</span><span class="sxs-lookup"><span data-stu-id="ab573-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="ab573-118">**Annulation de l’inscription d’un DMO**</span><span class="sxs-lookup"><span data-stu-id="ab573-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="ab573-119">Votre fonction **DllUnregisterServer** doit supprimer toutes les entrées de Registre créées par la fonction **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="ab573-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="ab573-120">Si vous appelez **DMORegister** lorsque vous inscrivez le DMO, vous devez [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) avec la même catégorie quand vous annulez l’inscription de la transaction DMO.</span><span class="sxs-lookup"><span data-stu-id="ab573-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="ab573-121">L’exemple suivant supprime les entrées de Registre créées dans l’exemple précédent :</span><span class="sxs-lookup"><span data-stu-id="ab573-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="ab573-122">**Valeurs des mérites DirectShow**</span><span class="sxs-lookup"><span data-stu-id="ab573-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="ab573-123">Dans le cadre de la création de graphiques de filtre, DirectShow attribue une valeur de mérite par défaut à DMOs.</span><span class="sxs-lookup"><span data-stu-id="ab573-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="ab573-124">Vous pouvez remplacer cette valeur en ajoutant une entrée de Registre à la clé de Registre DMO dans HKEY \_ classes \_ racine \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="ab573-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="ab573-125">Incluez une valeur **DWORD** nommée `Merit` dont la valeur spécifie le mérite.</span><span class="sxs-lookup"><span data-stu-id="ab573-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab573-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab573-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab573-127">Écriture d’un DMO</span><span class="sxs-lookup"><span data-stu-id="ab573-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



