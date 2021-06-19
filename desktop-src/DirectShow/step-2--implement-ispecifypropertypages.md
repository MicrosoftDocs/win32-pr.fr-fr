---
description: Implémentez l’interface ISpecifyPropertyPages dans votre filtre dans le cadre de la création d’une page de propriétés de filtre pour un filtre DirectShow personnalisé.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Étape 2. Implémenter ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410052"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="18cb9-104">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="18cb9-104">Step 2.</span></span> <span data-ttu-id="18cb9-105">Implémenter ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="18cb9-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="18cb9-106">Ensuite, implémentez l’interface **ISpecifyPropertyPages** dans votre filtre.</span><span class="sxs-lookup"><span data-stu-id="18cb9-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="18cb9-107">Cette interface possède une méthode unique, **GetPages**, qui retourne un tableau de CLSID pour les pages de propriétés prises en charge par le filtre.</span><span class="sxs-lookup"><span data-stu-id="18cb9-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="18cb9-108">Dans cet exemple, le filtre comporte une seule page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18cb9-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="18cb9-109">Commencez par générer le CLSID et en le déclarant dans votre fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="18cb9-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="18cb9-110">Implémentez maintenant la méthode **GetPages** :</span><span class="sxs-lookup"><span data-stu-id="18cb9-110">Now implement the **GetPages** method:</span></span>


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



<span data-ttu-id="18cb9-111">Allouez de la mémoire pour le tableau à l’aide de **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="18cb9-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="18cb9-112">L’appelant va libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="18cb9-112">The caller will release the memory.</span></span>

<span data-ttu-id="18cb9-113">Suivant : [étape 3. Prendre en charge QueryInterface](step-3--support-queryinterface.md).</span><span class="sxs-lookup"><span data-stu-id="18cb9-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18cb9-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18cb9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18cb9-115">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="18cb9-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



