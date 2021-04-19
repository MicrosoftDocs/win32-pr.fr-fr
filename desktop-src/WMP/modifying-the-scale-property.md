---
title: Modification de la propriété Scale
description: Modification de la propriété Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Plug-ins du lecteur Windows Media, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriété Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508974"
---
# <a name="modifying-the-scale-property"></a>Modification de la propriété Scale

L’implémentation de l’Assistant par défaut expose la propriété Scale. Vous pouvez modifier l’implémentation existante pour exposer la propriété Delay Time à la place.

Tout d’abord, utilisez l’exemple suivant pour modifier les prototypes de fonction pour les fonctions obtenir une \_ échelle et mettre \_ à l’échelle dans Echo. h. Modifiez le nom des méthodes et les types de données des paramètres :


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Ensuite, modifiez les implémentations des méthodes d’extraction d' \_ échelle et de mise \_ à l’échelle dans Echo. cpp. Faites en sorte que le code corresponde aux exemples suivants :


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



L’exemple de code précédent modifie les noms des méthodes et les types de données des paramètres. Le nom de la variable membre doit avoir été modifié précédemment. N’oubliez pas de modifier les commentaires qui introduisent chaque méthode également.

À présent, modifiez la définition de l’interface. Le code suivant remplace le code dans la déclaration de l’interface IEcho dans Echo. idl :


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples de propriétés Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




