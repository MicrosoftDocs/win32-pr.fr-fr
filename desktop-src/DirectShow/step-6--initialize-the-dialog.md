---
description: 'Substituez la méthode CBasePropertyPage :: OnActivate pour initialiser la boîte de dialogue dans le cadre de la création d’une page de propriétés de filtre pour un filtre DirectShow personnalisé.'
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Étape 6. Initialiser la boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbdf18e272ac548227626bc9da4f992786a4ab3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404492"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="38a58-104">Étape 6.</span><span class="sxs-lookup"><span data-stu-id="38a58-104">Step 6.</span></span> <span data-ttu-id="38a58-105">Initialiser la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="38a58-105">Initialize the Dialog</span></span>

<span data-ttu-id="38a58-106">Substituez la méthode [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md) pour initialiser la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38a58-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="38a58-107">Dans cet exemple, la page de propriétés utilise un contrôle Slider, donc la première étape de **OnActivate** consiste à initialiser la bibliothèque de contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="38a58-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="38a58-108">La méthode initialise ensuite le contrôle Slider à l’aide de la valeur actuelle de la propriété saturation du filtre :</span><span class="sxs-lookup"><span data-stu-id="38a58-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


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



<span data-ttu-id="38a58-109">Suivant : [étape 7. Gérer les messages de fenêtre](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="38a58-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="38a58-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38a58-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a58-111">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="38a58-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



