---
description: Explique comment modifier l’apparence du contrôle d’entrée mathématique.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personnalisation du contrôle d’entrée mathématique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565707"
---
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="95d09-103">Personnalisation du contrôle d’entrée mathématique</span><span class="sxs-lookup"><span data-stu-id="95d09-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="95d09-104">Il est possible de modifier l’apparence du contrôle d’entrée mathématique afin qu’il soit mieux adapté à votre application.</span><span class="sxs-lookup"><span data-stu-id="95d09-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="95d09-105">Cette rubrique explique les différentes façons dont les développeurs peuvent personnaliser le contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="95d09-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="95d09-106">Les personnalisations suivantes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="95d09-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="95d09-107">Modification des boutons affichés</span><span class="sxs-lookup"><span data-stu-id="95d09-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="95d09-108">Modification de la légende du contrôle</span><span class="sxs-lookup"><span data-stu-id="95d09-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="95d09-109">Modification de la taille de la zone d’aperçu du contrôle</span><span class="sxs-lookup"><span data-stu-id="95d09-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="95d09-110">Modification des boutons affichés</span><span class="sxs-lookup"><span data-stu-id="95d09-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="95d09-111">Vous pouvez modifier les boutons affichés dans le contrôle d’entrée mathématique afin que le contrôle dispose de fonctionnalités étendues ou soit plus petit à l’écran.</span><span class="sxs-lookup"><span data-stu-id="95d09-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="95d09-112">L’activation du jeu de boutons étendus affiche les boutons **rétablir** et **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="95d09-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="95d09-113">Le code suivant montre comment activer le jeu de boutons étendus.</span><span class="sxs-lookup"><span data-stu-id="95d09-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="95d09-114">L’illustration suivante montre le contrôle avec le jeu de boutons étendu.</span><span class="sxs-lookup"><span data-stu-id="95d09-114">The following image shows the control with the extended set of buttons.</span></span>

![contrôle d’entrée mathématique avec un ensemble étendu de boutons](images/mic.png)

<span data-ttu-id="95d09-116">L’illustration suivante montre le contrôle sans le jeu étendu de boutons.</span><span class="sxs-lookup"><span data-stu-id="95d09-116">The following image shows the control without the extended set of buttons.</span></span>

![contrôle d’entrée mathématique sans un ensemble étendu de boutons](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="95d09-118">Modification de la légende du contrôle</span><span class="sxs-lookup"><span data-stu-id="95d09-118">Changing the Control Caption</span></span>

<span data-ttu-id="95d09-119">Vous pouvez modifier la légende du contrôle pour le contrôle d’entrée mathématique afin de définir la légende dans la fenêtre du contrôle de saisie mathématique.</span><span class="sxs-lookup"><span data-stu-id="95d09-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="95d09-120">Le code suivant montre comment définir la légende.</span><span class="sxs-lookup"><span data-stu-id="95d09-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="95d09-121">L’illustration suivante montre le contrôle après la définition de la légende.</span><span class="sxs-lookup"><span data-stu-id="95d09-121">The following image shows the control after the caption has been set.</span></span>

![contrôle d’entrée mathématique avec une légende définie](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="95d09-123">Modification de la taille de la zone d’aperçu du contrôle</span><span class="sxs-lookup"><span data-stu-id="95d09-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="95d09-124">Vous pouvez personnaliser le contrôle d’entrée mathématique afin que le contrôle définisse explicitement sa taille de zone d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="95d09-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="95d09-125">Cela crée une zone plus grande dans laquelle les formules mathématiques sont affichées.</span><span class="sxs-lookup"><span data-stu-id="95d09-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="95d09-126">Le code suivant montre comment définir la taille de la zone d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="95d09-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="95d09-127">Les images suivantes montrent un contrôle avec des zones d’aperçu de taille différente.</span><span class="sxs-lookup"><span data-stu-id="95d09-127">The following images show a control with differently sized preview areas.</span></span>

![contrôle d’entrée mathématique avec la taille de zone d’aperçu par défaut](images/mic.png)![contrôle d’entrée mathématique avec une plus grande zone d’aperçu](images/mic-big-preview.png)

 

 



