---
description: Étape 6.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Étape 6. Initialiser la boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282eb03db38c543678fb2c4ef1155e1150b419bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529368"
---
# <a name="step-6-initialize-the-dialog"></a>Étape 6. Initialiser la boîte de dialogue

Substituez la méthode [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md) pour initialiser la boîte de dialogue. Dans cet exemple, la page de propriétés utilise un contrôle Slider, donc la première étape de **OnActivate** consiste à initialiser la bibliothèque de contrôles communs. La méthode initialise ensuite le contrôle Slider à l’aide de la valeur actuelle de la propriété saturation du filtre :


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



Suivant : [étape 7. Gérer les messages de fenêtre](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



