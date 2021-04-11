---
description: Étape 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Étape 5. Stocker un pointeur vers le filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209729"
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

 

 



