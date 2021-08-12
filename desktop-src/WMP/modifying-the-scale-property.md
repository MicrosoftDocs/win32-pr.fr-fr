---
title: Modification de la propriété Scale
description: Modification de la propriété Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Lecteur Windows Media les plug-ins, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriété Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10073e01213469dcb6a85ddffd378421fddb6ae8f2fd432b9822c3a5046fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574616"
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

 

 




