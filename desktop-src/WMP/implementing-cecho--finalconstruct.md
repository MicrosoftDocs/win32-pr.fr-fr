---
title: Implémentation de CEcho FinalConstruct
description: Implémentation de CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, CEcho FinalConstruct, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100689"
---
# <a name="implementing-cechofinalconstruct"></a><span data-ttu-id="46a6a-109">Implémentation de CEcho :: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="46a6a-109">Implementing CEcho::FinalConstruct</span></span>

<span data-ttu-id="46a6a-110">La méthode CEcho :: FinalConstruct est implémentée dans Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="46a6a-110">The CEcho::FinalConstruct method is implemented in Echo.cpp.</span></span> <span data-ttu-id="46a6a-111">Il contient le code permettant de lire les valeurs de propriété à partir du registre lorsque le lecteur Windows Media instancie l’objet de plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="46a6a-111">It contains code to read the property values from the registry when Windows Media Player instantiates the DSP plug-in object.</span></span> <span data-ttu-id="46a6a-112">Cela est important, car il permet aux paramètres utilisateur de persister entre les instances de l’objet, ainsi qu’entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="46a6a-112">This is important because it allows the user settings to persist between instances of the object, as well as between sessions.</span></span> <span data-ttu-id="46a6a-113">L’exemple de code de l’Assistant de plug-in fournit une implémentation pour lire une seule propriété à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="46a6a-113">The plug-in wizard sample code provides implementation to read a single property from the registry.</span></span> <span data-ttu-id="46a6a-114">Vous pouvez modifier ce code pour gérer la propriété Delay Time, puis ajouter du code pour lire la valeur de la propriété de combinaison humide.</span><span class="sxs-lookup"><span data-stu-id="46a6a-114">You can modify this code to handle the delay time property, and then add code to read the wet mix property value.</span></span>

<span data-ttu-id="46a6a-115">L’exemple de code suivant lit chaque valeur de propriété à partir du Registre et les stocke dans la variable de membre appropriée :</span><span class="sxs-lookup"><span data-stu-id="46a6a-115">The following example code reads each property value from the registry and stores each in the correct member variable:</span></span>


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



<span data-ttu-id="46a6a-116">Notez que la valeur DWORD pour la combinaison humide est convertie en valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="46a6a-116">Notice that the DWORD value for the wet mix is converted to a floating-point value.</span></span> <span data-ttu-id="46a6a-117">Notez également que le code calcule la valeur correcte pour m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="46a6a-117">Also note that the code calculates the correct value for m\_fDryMix.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a6a-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46a6a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a6a-119">**Modification de la page de propriétés de l’exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="46a6a-119">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




