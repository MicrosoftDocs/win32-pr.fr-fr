---
title: Comment utiliser les méthodes de tabulation dans TOM
description: L’exemple suivant fournit des fonctions C qui illustrent l’utilisation des méthodes d’onglet dans le modèle d’objet de texte (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841997"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Comment utiliser les méthodes de tabulation dans TOM

L’exemple suivant fournit des fonctions C qui illustrent l’utilisation des méthodes d’onglet dans le modèle d’objet de texte (TOM). Il est supposé que la plupart des applications incluent une barre d’outils qui indique la position actuelle et le type des onglets pour le paragraphe actuellement sélectionné.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="use-a-tab-method"></a>Utiliser une méthode Tab

L’exemple de code suivant montre comment mettre à jour une barre d’outils avec les détails de l’onglet actuel.


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a>Copier les informations de l’onglet

L’exemple suivant montre comment copier uniquement les informations d’onglet d’une interface [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) vers une autre. Il accepte deux paramètres : **ITextPara** \* *pParaFrom* (le paragraphe à partir duquel copier les tabulations) et **ITextPara** \* *pParaFrom* (le paragraphe dans lequel copier les tabulations).


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du modèle d’objet de texte](using-the-text-object-model.md)
</dt> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




