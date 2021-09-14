---
description: définissez un mécanisme pour définir la propriété dans le cadre de la création d’une page de propriétés de filtre pour un filtre de DirectShow personnalisé.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Étape 1. Définir un mécanisme pour définir la propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094646"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Étape 1. Définir un mécanisme pour définir la propriété

Le filtre doit prendre en charge un moyen pour la page de propriétés de communiquer avec lui, afin que la page de propriétés puisse définir et récupérer des propriétés sur le filtre. Les mécanismes possibles sont les suivants :

-   Exposer une interface COM personnalisée.
-   Prendre en charge les propriétés d’automatisation, via **IDispatch**.
-   Exposer l’interface **IPropertyBag** et définir un ensemble de propriétés nommées.

Cet exemple utilise une interface COM personnalisée, nommée ISaturation. il ne s’agit pas d’une interface DirectShow réelle ; elle est définie uniquement pour cet exemple. Commencez par déclarer l’interface dans un fichier d’en-tête, avec l’identificateur d’interface (IID) :


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



Vous pouvez également définir l’interface avec IDL et utiliser le compilateur MIDL pour créer le fichier d’en-tête. Ensuite, implémentez l’interface personnalisée dans le filtre. Cet exemple utilise les méthodes « obtenir » et « définir » pour la valeur de saturation du filtre. Notez que les deux méthodes protègent le \_ membre m lSaturation avec une section critique.


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



Bien entendu, les détails de votre propre implémentation diffèrent de l’exemple présenté ici.

Suivant : [étape 2. Implémentez ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



