---
description: Étape 2.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Étape 2. Implémenter ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540887"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="8f839-104">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="8f839-104">Step 2.</span></span> <span data-ttu-id="8f839-105">Implémenter ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="8f839-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="8f839-106">Ensuite, implémentez l’interface **ISpecifyPropertyPages** dans votre filtre.</span><span class="sxs-lookup"><span data-stu-id="8f839-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="8f839-107">Cette interface possède une méthode unique, **GetPages**, qui retourne un tableau de CLSID pour les pages de propriétés prises en charge par le filtre.</span><span class="sxs-lookup"><span data-stu-id="8f839-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="8f839-108">Dans cet exemple, le filtre comporte une seule page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8f839-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="8f839-109">Commencez par générer le CLSID et en le déclarant dans votre fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8f839-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="8f839-110">Implémentez maintenant la méthode **GetPages** :</span><span class="sxs-lookup"><span data-stu-id="8f839-110">Now implement the **GetPages** method:</span></span>


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



<span data-ttu-id="8f839-111">Allouez de la mémoire pour le tableau à l’aide de **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="8f839-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="8f839-112">L’appelant va libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8f839-112">The caller will release the memory.</span></span>

<span data-ttu-id="8f839-113">Suivant : [étape 3. Prendre en charge QueryInterface](step-3--support-queryinterface.md).</span><span class="sxs-lookup"><span data-stu-id="8f839-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f839-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f839-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f839-115">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="8f839-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



