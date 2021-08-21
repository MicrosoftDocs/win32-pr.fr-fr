---
description: Étape 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Étape 9. Déconnecter la page de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf4bcb670b8a8f29334f7ecd41ebba37a915f724be70e5dbbbfd7abea9730be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526080"
---
# <a name="step-9-disconnect-the-property-page"></a>Étape 9. Déconnecter la page de propriétés

Substituez la méthode [**CBasePropertyPage :: OnDisconnect**](cbasepropertypage-ondisconnect.md) pour libérer toutes les interfaces obtenues dans la méthode **OnConnect** . En outre, si l’utilisateur ignore la feuille de propriétés sans valider les modifications, vous devez restaurer les valeurs d’origine si elles ont été modifiées. Il n’existe aucune méthode « OnCancel » appelée lorsque l’utilisateur annule. vous devez donc effectuer le suivi du fait que l’utilisateur a appelé **OnApplyChanges**. Cet exemple utilise la \_ variable m lVal, décrite précédemment :


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



Ensuite : [étape 10. Prise en charge de l’inscription COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



