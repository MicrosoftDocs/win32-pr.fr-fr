---
title: Variables pour stocker les propriétés
description: Variables pour stocker les propriétés
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Plug-ins du lecteur Windows Media, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriétés
- Echo DSP, exemple de plug-in, variables pour le stockage des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196939"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="feb0d-109">Variables pour stocker les propriétés</span><span class="sxs-lookup"><span data-stu-id="feb0d-109">Variables to Store Properties</span></span>

<span data-ttu-id="feb0d-110">Tout d’abord, vous aurez besoin d’une variable pour stocker le temps de retard.</span><span class="sxs-lookup"><span data-stu-id="feb0d-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="feb0d-111">L’exemple par défaut créé par l’Assistant de plug-in du lecteur Windows Media fournit une variable nommée m \_ fScaleFactor pour stocker le multiplicateur de mise à l’échelle qu’il utilise pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="feb0d-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="feb0d-112">Cet exemple n’a plus besoin de cette variable. vous pouvez donc modifier son nom et son type pour stocker la valeur de délai.</span><span class="sxs-lookup"><span data-stu-id="feb0d-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="feb0d-113">Remplacez chaque instance de m \_ fScaleFactor dans Echo. h et Echo. cpp par m \_ dwDelayTime.</span><span class="sxs-lookup"><span data-stu-id="feb0d-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="feb0d-114">Remplacez le type de données de m \_ fScaleFactor (Now m \_ dwDelayTime) de double par DWORD dans Echo. h.</span><span class="sxs-lookup"><span data-stu-id="feb0d-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="feb0d-115">Dans le constructeur de CEcho, remplacez la valeur de délai par défaut par 1000.</span><span class="sxs-lookup"><span data-stu-id="feb0d-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="feb0d-116">Ensuite, déclarez deux nouvelles variables membres pour stocker le pourcentage de signal d’effet et le pourcentage de signal source à mélanger dans la mémoire tampon de sortie finale.</span><span class="sxs-lookup"><span data-stu-id="feb0d-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="feb0d-117">Le terme « mouillé » fait référence à l’effet et le terme « secs » fait référence au signal source.</span><span class="sxs-lookup"><span data-stu-id="feb0d-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="feb0d-118">Ajoutez les déclarations suivantes à ECHO. h :</span><span class="sxs-lookup"><span data-stu-id="feb0d-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="feb0d-119">Ces valeurs sont stockées sous forme de représentations décimales de pourcentages afin d’être facilement utilisées comme facteurs de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="feb0d-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="feb0d-120">Par exemple, un mélange d’effets de 50% et de signal source de 50% serait représenté comme valeur de 0,50 pour chaque variable.</span><span class="sxs-lookup"><span data-stu-id="feb0d-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="feb0d-121">La somme des valeurs pour m \_ fWetMix et m \_ fDryMix ne doit pas être supérieure à 1,0 (100 pour cent).</span><span class="sxs-lookup"><span data-stu-id="feb0d-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="feb0d-122">Finalement, ces valeurs sont accessibles en tant que propriétés.</span><span class="sxs-lookup"><span data-stu-id="feb0d-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="feb0d-123">Ajoutez le code suivant au constructeur CEcho pour définir les valeurs par défaut à 50 pour cent chacune :</span><span class="sxs-lookup"><span data-stu-id="feb0d-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="feb0d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="feb0d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb0d-125">**Exemples de propriétés Echo**</span><span class="sxs-lookup"><span data-stu-id="feb0d-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




