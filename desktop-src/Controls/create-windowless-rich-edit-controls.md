---
title: Comment fournir des contrôles RichEdit sans fenêtre avec des fonctionnalités de fenêtre
description: La fonctionnalité de fenêtre offre la possibilité de recevoir des messages et la propriété d’un contexte de périphérique dans lequel dessiner. Les contrôles RichEdit sans fenêtre reçoivent cette fonctionnalité par le biais d’une paire d’interfaces ITextServices et ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce68a9e4e186be79e8f62cb009748916725e4af4f67d6522ed5eb47a92f33fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698599"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Comment fournir des contrôles RichEdit sans fenêtre avec des fonctionnalités de fenêtre

La fonctionnalité de fenêtre offre la possibilité de recevoir des messages et la propriété d’un contexte de périphérique dans lequel dessiner. Les contrôles RichEdit sans fenêtre reçoivent cette fonctionnalité par le biais d’une paire d’interfaces : [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) et [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="establish-the-window-functionality"></a>Établir les fonctionnalités de la fenêtre

L’exemple de code suivant montre comment créer l’hôte de texte et les services de texte.


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a>Remarques

Le paramètre *hmodRichEdit* dans l’exemple de code est un handle vers le module Msftedit.dll, et il est supposé que ce descripteur a déjà été récupéré par un appel à la fonction **GetModuleHandle** .

## <a name="complete-example"></a>Exemple complet

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit sans fenêtre](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




