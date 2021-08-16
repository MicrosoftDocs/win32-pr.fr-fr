---
title: Comment utiliser les méthodes de tabulation dans TOM
description: L’exemple suivant fournit des fonctions C qui illustrent l’utilisation des méthodes d’onglet dans le modèle d’objet de texte (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b4a101c2deb3c22993f41b11ee94df6ac738da41963046f02a072f3eaa6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828611"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Comment utiliser les méthodes de tabulation dans TOM

L’exemple suivant fournit des fonctions C qui illustrent l’utilisation des méthodes d’onglet dans le modèle d’objet de texte (TOM). Il est supposé que la plupart des applications incluent une barre d’outils qui indique la position actuelle et le type des onglets pour le paragraphe actuellement sélectionné.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

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

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




