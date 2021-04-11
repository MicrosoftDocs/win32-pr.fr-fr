---
title: Ajout de la propriété de combinaison humide
description: Ajout de la propriété de combinaison humide
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Plug-ins du lecteur Windows Media, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriétés
- Echo DSP, exemple de plug-in, propriété de combinaison humide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310089"
---
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="fea48-109">Ajout de la propriété de combinaison humide</span><span class="sxs-lookup"><span data-stu-id="fea48-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="fea48-110">Vous devez ajouter le code pour fournir la propriété supplémentaire pour le niveau d’effet.</span><span class="sxs-lookup"><span data-stu-id="fea48-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="fea48-111">La section [Ajout de propriétés à l’exemple de plug-in DSP audio](adding-properties-to-the-sample-audio-dsp-plug-in.md) fournit des détails sur l’ajout d’une nouvelle propriété à l’aide de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="fea48-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="fea48-112">Cette section vous montre comment ajouter le code manuellement.</span><span class="sxs-lookup"><span data-stu-id="fea48-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="fea48-113">Cela implique l’ajout de code dans les trois emplacements où vous avez modifié le code pour la propriété Delay Time.</span><span class="sxs-lookup"><span data-stu-id="fea48-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="fea48-114">Ajoutez les prototypes pour les \_ méthodes obtenir WETMIX et put \_ WETMIX immédiatement après les autres prototypes de méthode de propriété dans Echo. h.</span><span class="sxs-lookup"><span data-stu-id="fea48-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="fea48-115">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fea48-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="fea48-116">Maintenant, ajoutez l’implémentation pour chaque méthode qui suit immédiatement les autres implémentations de propriété dans Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="fea48-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="fea48-117">L’exemple suivant montre le code pour les deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="fea48-117">The following example shows the code for both methods:</span></span>


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



<span data-ttu-id="fea48-118">Notez que l’implémentation de put \_ WETMIX comprend le code permettant de calculer la valeur correcte pour m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="fea48-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="fea48-119">À chaque fois qu’une nouvelle valeur est spécifiée pour m \_ fWetMix, ce calcul est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fea48-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="fea48-120">Ajoutez le code suivant dans la définition de l’interface juste après le code pour les méthodes Delay dans Echo. idl :</span><span class="sxs-lookup"><span data-stu-id="fea48-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="fea48-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fea48-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea48-122">**Exemples de propriétés Echo**</span><span class="sxs-lookup"><span data-stu-id="fea48-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




