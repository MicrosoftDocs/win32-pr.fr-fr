---
description: implémentez l’interface ISpecifyPropertyPages dans votre filtre dans le cadre de la création d’une page de propriétés de filtre pour un filtre de DirectShow personnalisé.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Étape 2. Implémenter ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2d1df86ef6e8b3e59f14a3efe1708a286761c9ba6425a7710a692ed6dcd3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951848"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Étape 2. Implémenter ISpecifyPropertyPages

Ensuite, implémentez l’interface **ISpecifyPropertyPages** dans votre filtre. Cette interface possède une méthode unique, **GetPages**, qui retourne un tableau de CLSID pour les pages de propriétés prises en charge par le filtre. Dans cet exemple, le filtre comporte une seule page de propriétés. Commencez par générer le CLSID et en le déclarant dans votre fichier d’en-tête :


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Implémentez maintenant la méthode **GetPages** :


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Allouez de la mémoire pour le tableau à l’aide de **CoTaskMemAlloc**. L’appelant va libérer de la mémoire.

Suivant : [étape 3. Prendre en charge QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



