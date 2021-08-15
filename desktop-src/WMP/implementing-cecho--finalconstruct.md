---
title: Implémentation de CEcho FinalConstruct
description: Implémentation de CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- plug-ins Lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, CEcho FinalConstruct, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeceeb9c0a7622ada62e98000ad4bfbc2e3faf08c22439039160810771cde8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748144"
---
# <a name="implementing-cechofinalconstruct"></a>Implémentation de CEcho :: FinalConstruct

La méthode CEcho :: FinalConstruct est implémentée dans Echo. cpp. il contient le code permettant de lire les valeurs de propriété à partir du registre lorsque Lecteur Windows Media instancie l’objet de plug-in DSP. Cela est important, car il permet aux paramètres utilisateur de persister entre les instances de l’objet, ainsi qu’entre les sessions. L’exemple de code de l’Assistant de plug-in fournit une implémentation pour lire une seule propriété à partir du Registre. Vous pouvez modifier ce code pour gérer la propriété Delay Time, puis ajouter du code pour lire la valeur de la propriété de combinaison humide.

L’exemple de code suivant lit chaque valeur de propriété à partir du Registre et les stocke dans la variable de membre appropriée :


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



Notez que la valeur DWORD pour la combinaison humide est convertie en valeur à virgule flottante. Notez également que le code calcule la valeur correcte pour m \_ fDryMix.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification de la page de propriétés de l’exemple Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




