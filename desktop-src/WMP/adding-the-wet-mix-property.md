---
title: Ajout de la propriété de combinaison humide
description: Ajout de la propriété de combinaison humide
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Lecteur Windows Media les plug-ins, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriétés
- Echo DSP, exemple de plug-in, propriété de combinaison humide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856347"
---
# <a name="adding-the-wet-mix-property"></a>Ajout de la propriété de combinaison humide

Vous devez ajouter le code pour fournir la propriété supplémentaire pour le niveau d’effet.

La section [Ajout de propriétés à l’exemple de plug-in DSP audio](adding-properties-to-the-sample-audio-dsp-plug-in.md) fournit des détails sur l’ajout d’une nouvelle propriété à l’aide de Visual C++. Cette section vous montre comment ajouter le code manuellement. Cela implique l’ajout de code dans les trois emplacements où vous avez modifié le code pour la propriété Delay Time.

Ajoutez les prototypes pour les \_ méthodes obtenir WETMIX et put \_ WETMIX immédiatement après les autres prototypes de méthode de propriété dans Echo. h. Utilisez la syntaxe suivante :


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Maintenant, ajoutez l’implémentation pour chaque méthode qui suit immédiatement les autres implémentations de propriété dans Echo. cpp. L’exemple suivant montre le code pour les deux méthodes :


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



Notez que l’implémentation de put \_ WETMIX comprend le code permettant de calculer la valeur correcte pour m \_ fDryMix. À chaque fois qu’une nouvelle valeur est spécifiée pour m \_ fWetMix, ce calcul est nécessaire.

Ajoutez le code suivant dans la définition de l’interface juste après le code pour les méthodes Delay dans Echo. idl :


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples de propriétés Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




