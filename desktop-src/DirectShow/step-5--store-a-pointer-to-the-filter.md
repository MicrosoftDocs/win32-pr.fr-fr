---
description: stocke un pointeur vers un filtre dans le cadre de la création d’une page de propriétés de filtre pour un filtre de DirectShow personnalisé.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Étape 5. Stocker un pointeur vers le filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63becf4cb98f401a4810f0f9a2604ef65387a58d08d84b9f670c09b51fe9acd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078769"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Étape 5. Stocker un pointeur vers le filtre

Substituez la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) pour stocker un pointeur vers le filtre. L’exemple suivant interroge le paramètre *punk* de l’interface ISaturation personnalisée du filtre :


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



Suivant : [étape 6. Initialisez la boîte de dialogue](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



