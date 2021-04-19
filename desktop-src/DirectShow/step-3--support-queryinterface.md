---
description: Étape 3.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Étape 3. Prendre en charge QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520721"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="4317b-104">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="4317b-104">Step 3.</span></span> <span data-ttu-id="4317b-105">Prendre en charge QueryInterface</span><span class="sxs-lookup"><span data-stu-id="4317b-105">Support QueryInterface</span></span>

<span data-ttu-id="4317b-106">Pour exposer les nouvelles interfaces du filtre aux clients, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4317b-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="4317b-107">Incluez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section Déclaration publique de votre filtre :</span><span class="sxs-lookup"><span data-stu-id="4317b-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="4317b-108">Remplacez [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour vérifier les IID des deux interfaces :</span><span class="sxs-lookup"><span data-stu-id="4317b-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

<span data-ttu-id="4317b-109">Suivant : [étape 4. Créez la page de propriétés](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="4317b-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4317b-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4317b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4317b-111">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="4317b-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="4317b-112">Comment implémenter IUnknown</span><span class="sxs-lookup"><span data-stu-id="4317b-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



