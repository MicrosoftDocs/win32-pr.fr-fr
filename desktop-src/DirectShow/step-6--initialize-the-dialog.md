---
description: 'substituez la méthode CBasePropertyPage :: OnActivate pour initialiser la boîte de dialogue dans le cadre de la création d’une page de propriétés de filtre pour un filtre de DirectShow personnalisé.'
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Étape 6. Initialiser la boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2ac2dbc4e8ed59317db3db46079b087e4afcf0fa8dce315aa2a0cbd45d502a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102309"
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

 

 



