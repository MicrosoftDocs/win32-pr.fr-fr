---
description: Étape 1.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Étape 1. Définir un mécanisme pour définir la propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521043"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="c94c6-104">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="c94c6-104">Step 1.</span></span> <span data-ttu-id="c94c6-105">Définir un mécanisme pour définir la propriété</span><span class="sxs-lookup"><span data-stu-id="c94c6-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="c94c6-106">Le filtre doit prendre en charge un moyen pour la page de propriétés de communiquer avec lui, afin que la page de propriétés puisse définir et récupérer des propriétés sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="c94c6-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="c94c6-107">Les mécanismes possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c94c6-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="c94c6-108">Exposer une interface COM personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c94c6-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="c94c6-109">Prendre en charge les propriétés d’automatisation, via **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="c94c6-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="c94c6-110">Exposer l’interface **IPropertyBag** et définir un ensemble de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="c94c6-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="c94c6-111">Cet exemple utilise une interface COM personnalisée, nommée ISaturation.</span><span class="sxs-lookup"><span data-stu-id="c94c6-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="c94c6-112">Il ne s’agit pas d’une interface DirectShow réelle. elle est définie uniquement pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="c94c6-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="c94c6-113">Commencez par déclarer l’interface dans un fichier d’en-tête, avec l’identificateur d’interface (IID) :</span><span class="sxs-lookup"><span data-stu-id="c94c6-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="c94c6-114">Vous pouvez également définir l’interface avec IDL et utiliser le compilateur MIDL pour créer le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c94c6-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="c94c6-115">Ensuite, implémentez l’interface personnalisée dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="c94c6-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="c94c6-116">Cet exemple utilise les méthodes « obtenir » et « définir » pour la valeur de saturation du filtre.</span><span class="sxs-lookup"><span data-stu-id="c94c6-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="c94c6-117">Notez que les deux méthodes protègent le \_ membre m lSaturation avec une section critique.</span><span class="sxs-lookup"><span data-stu-id="c94c6-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="c94c6-118">Bien entendu, les détails de votre propre implémentation diffèrent de l’exemple présenté ici.</span><span class="sxs-lookup"><span data-stu-id="c94c6-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="c94c6-119">Suivant : [étape 2. Implémentez ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="c94c6-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c94c6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c94c6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c94c6-121">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="c94c6-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="c94c6-122">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="c94c6-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



