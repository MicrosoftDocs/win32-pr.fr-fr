---
description: Stocke un pointeur vers un filtre dans le cadre de la création d’une page de propriétés de filtre pour un filtre DirectShow personnalisé.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Étape 5. Stocker un pointeur vers le filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406792"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="ea015-104">Étape 5.</span><span class="sxs-lookup"><span data-stu-id="ea015-104">Step 5.</span></span> <span data-ttu-id="ea015-105">Stocker un pointeur vers le filtre</span><span class="sxs-lookup"><span data-stu-id="ea015-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="ea015-106">Substituez la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) pour stocker un pointeur vers le filtre.</span><span class="sxs-lookup"><span data-stu-id="ea015-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="ea015-107">L’exemple suivant interroge le paramètre *punk* de l’interface ISaturation personnalisée du filtre :</span><span class="sxs-lookup"><span data-stu-id="ea015-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



<span data-ttu-id="ea015-108">Suivant : [étape 6. Initialisez la boîte de dialogue](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="ea015-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea015-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea015-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea015-110">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="ea015-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



