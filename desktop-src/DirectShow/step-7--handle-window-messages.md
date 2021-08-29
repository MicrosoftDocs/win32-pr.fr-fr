---
description: Étape 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Étape 7. Gérer les messages de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f1aa28e891dfce8715984f505d6177c75ba6dc21ed8290c6e2bebee2e8203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102299"
---
# <a name="step-7-handle-window-messages"></a>Étape 7. Gérer les messages de fenêtre

Substituez la méthode [**CBasePropertyPage :: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) pour mettre à jour les contrôles de boîte de dialogue en réponse à l’entrée utilisateur. Si vous ne gérez pas un message particulier, appelez la méthode **OnReceiveMessage** sur la classe parente. Chaque fois que l’utilisateur modifie une propriété, procédez comme suit :

-   Affectez la valeur **true** à la variable **m \_ bDirty** de la page de propriétés.
-   Appelez la méthode **IPropertyPageSite :: OnStatusChange** du frame de propriété avec l' \_ indicateur de modification PROPPAGESTATUS. Cet indicateur informe le frame de propriété qu’il doit activer le bouton **appliquer** . Le membre [**CBasePropertyPage :: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) contient un pointeur vers l’interface **IPropertyPageSite** .

Pour simplifier cette étape, vous pouvez ajouter la fonction d’assistance suivante à la page de propriétés :


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



Appelez cette méthode privée à l’intérieur de **OnReceiveMessage** chaque fois qu’une action de l’utilisateur modifie une propriété, comme illustré dans l’exemple suivant :


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



Dans cet exemple, la page de propriétés contient deux contrôles, une barre de curseur et un bouton **rétablir les valeurs par défaut** . Si l’utilisateur fait défiler la barre du curseur, la page de propriétés définit la valeur de saturation sur le filtre. Si l’utilisateur clique sur le bouton, la page de propriétés restaure la valeur de saturation par défaut du filtre. Dans chaque cas, m \_ lNewVal contient la valeur actuelle et m \_ lVal contient la valeur d’origine. La valeur de m \_ lVal n’est pas mise à jour tant que l’utilisateur n’a pas validé la modification, ce qui se produit lorsque l’utilisateur clique sur le bouton **OK** ou **appliquer** du frame de propriété.

Étape suivante : [étape 8. Appliquer les modifications de propriété](step-8--apply-property-changes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



