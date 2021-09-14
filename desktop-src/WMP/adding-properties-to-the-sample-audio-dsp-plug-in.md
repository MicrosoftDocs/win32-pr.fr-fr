---
title: Ajout de propriétés à l’exemple de plug-in DSP audio
description: Ajout de propriétés à l’exemple de plug-in DSP audio
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, propriétés audio
- Plug-ins DSP, propriétés audio
- plug-ins DSP audio, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324294"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Ajout de propriétés à l’exemple de plug-in DSP audio

l’exemple de code DSP audio généré par l’assistant de Plug-in Lecteur Windows Media utilise une propriété unique qui représente le facteur d’échelle du volume audio. Votre plug-in peut nécessiter plus d’une propriété. vous pouvez facilement ajouter des propriétés à votre plug-in DSP dans Visual Studio en procédant comme suit :

-   Définissez les méthodes dans le code de définition d’interface dans le fichier IDL qui fait partie du projet proxy-stub.
    -   Ajoutez les implémentations de méthode au fichier CPP principal du projet :

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

Enfin, pour rendre les propriétés accessibles à l’utilisateur, vous devez apporter des modifications à l’implémentation de la page de propriétés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




