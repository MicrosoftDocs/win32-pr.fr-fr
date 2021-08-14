---
description: Explique comment modifier l’apparence du contrôle d’entrée mathématique.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personnalisation du contrôle d’entrée mathématique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adedc4ab5b655f4f753a1b83cabe28e322adaad3c73bcf9f25ea1dea6d0bc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045626"
---
# <a name="customizing-the-math-input-control"></a>Personnalisation du contrôle d’entrée mathématique

Il est possible de modifier l’apparence du contrôle d’entrée mathématique afin qu’il soit mieux adapté à votre application. Cette rubrique explique les différentes façons dont les développeurs peuvent personnaliser le contrôle d’entrée mathématique.

Les personnalisations suivantes sont possibles :

-   [Modification des boutons affichés](#changing-the-displayed-buttons)
-   [Modification de la légende du contrôle](#changing-the-control-caption)
-   [Modification de la taille de la zone d’aperçu du contrôle](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Modification des boutons affichés

Vous pouvez modifier les boutons affichés dans le contrôle d’entrée mathématique afin que le contrôle dispose de fonctionnalités étendues ou soit plus petit à l’écran. L’activation du jeu de boutons étendus affiche les boutons **rétablir** et **Annuler** . Le code suivant montre comment activer le jeu de boutons étendus.


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



L’illustration suivante montre le contrôle avec le jeu de boutons étendu.

![contrôle d’entrée mathématique avec un ensemble étendu de boutons](images/mic.png)

L’illustration suivante montre le contrôle sans le jeu étendu de boutons.

![contrôle d’entrée mathématique sans un ensemble étendu de boutons](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Modification de la légende du contrôle

Vous pouvez modifier la légende du contrôle pour le contrôle d’entrée mathématique afin de définir la légende dans la fenêtre du contrôle de saisie mathématique. Le code suivant montre comment définir la légende.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



L’illustration suivante montre le contrôle après la définition de la légende.

![contrôle d’entrée mathématique avec une légende définie](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Modification de la taille de la zone d’aperçu du contrôle

Vous pouvez personnaliser le contrôle d’entrée mathématique afin que le contrôle définisse explicitement sa taille de zone d’aperçu. Cela crée une zone plus grande dans laquelle les formules mathématiques sont affichées. Le code suivant montre comment définir la taille de la zone d’aperçu.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



Les images suivantes montrent un contrôle avec des zones d’aperçu de taille différente.

![contrôle d’entrée mathématique avec la taille de zone d’aperçu par défaut](images/mic.png)![contrôle d’entrée mathématique avec une plus grande zone d’aperçu](images/mic-big-preview.png)

 

 



