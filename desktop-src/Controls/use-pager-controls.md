---
title: Comment utiliser les contrôles de pagineur
description: Cette section décrit comment implémenter le contrôle de pagineur dans votre application.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031940"
---
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="ff94b-103">Comment utiliser les contrôles de pagineur</span><span class="sxs-lookup"><span data-stu-id="ff94b-103">How to Use Pager Controls</span></span>

<span data-ttu-id="ff94b-104">Cette section décrit comment implémenter le contrôle de pagineur dans votre application.</span><span class="sxs-lookup"><span data-stu-id="ff94b-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ff94b-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="ff94b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ff94b-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="ff94b-106">Technologies</span></span>

-   [<span data-ttu-id="ff94b-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="ff94b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ff94b-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ff94b-108">Prerequisites</span></span>

-   <span data-ttu-id="ff94b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff94b-109">C/C++</span></span>
-   <span data-ttu-id="ff94b-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="ff94b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ff94b-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="ff94b-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="ff94b-112">Initialiser un contrôle de pagineur</span><span class="sxs-lookup"><span data-stu-id="ff94b-112">Initialize a Pager Control</span></span>

<span data-ttu-id="ff94b-113">Pour utiliser le contrôle de pagineur, vous devez appeler la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) avec l' \_ indicateur de classe PAGESCROLLER ICC \_ défini dans le membre **dwICC** de la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="ff94b-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="ff94b-114">Créer un contrôle de pagineur</span><span class="sxs-lookup"><span data-stu-id="ff94b-114">Create a Pager Control</span></span>

<span data-ttu-id="ff94b-115">Utilisez l’API [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="ff94b-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="ff94b-116">Le nom de classe du contrôle est [**WC \_ PAGESCROLLER**](common-control-window-classes.md), qui est défini dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="ff94b-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="ff94b-117">Le [**style \_ Horiz PG**](pager-control-styles.md) est utilisé pour créer un pagineur horizontal et le style [**PG \_ vert**](pager-control-styles.md) est utilisé pour créer un pagineur vertical.</span><span class="sxs-lookup"><span data-stu-id="ff94b-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="ff94b-118">Étant donné qu’il s’agit d’un contrôle enfant, le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) doit également être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff94b-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="ff94b-119">Une fois le contrôle de pagineur créé, vous souhaiterez probablement lui assigner une fenêtre qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="ff94b-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="ff94b-120">Si la fenêtre contenue est une fenêtre enfant, vous devez faire de la fenêtre enfant un enfant du contrôle de pagineur afin que la taille et la position soient calculées correctement.</span><span class="sxs-lookup"><span data-stu-id="ff94b-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="ff94b-121">Vous assignez ensuite la fenêtre au contrôle pager avec le message [**PGM \_ SETCHILD**](pgm-setchild.md) .</span><span class="sxs-lookup"><span data-stu-id="ff94b-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="ff94b-122">N’oubliez pas que ce message ne modifie pas réellement la fenêtre parente de la fenêtre contenue ; elle affecte simplement la fenêtre contenue.</span><span class="sxs-lookup"><span data-stu-id="ff94b-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="ff94b-123">Si la fenêtre contenue est l’un des contrôles communs, elle doit avoir le style [**CCS \_ NORESIZE**](common-control-styles.md) pour empêcher le contrôle d’essayer de se redimensionner à la taille du contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="ff94b-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="ff94b-124">Traiter les notifications de contrôle de pagineur</span><span class="sxs-lookup"><span data-stu-id="ff94b-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="ff94b-125">Au minimum, il est nécessaire de traiter la notification [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="ff94b-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="ff94b-126">Si vous ne traitez pas cette notification et que vous entrez une valeur pour la largeur ou la hauteur, les flèches de défilement dans le contrôle de pagineur ne seront pas affichées.</span><span class="sxs-lookup"><span data-stu-id="ff94b-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="ff94b-127">Cela est dû au fait que le contrôle de pagineur utilise la largeur ou la hauteur fournie dans la \_ notification CALCSIZE PGN pour déterminer la taille idéale de la fenêtre contenue.</span><span class="sxs-lookup"><span data-stu-id="ff94b-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="ff94b-128">L’exemple suivant montre comment traiter le cas de notification [ \_ CALCSIZE PGN](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="ff94b-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="ff94b-129">Dans cet exemple, la fenêtre contenue est un contrôle de barre d’outils qui contient un nombre inconnu de boutons à une taille inconnue.</span><span class="sxs-lookup"><span data-stu-id="ff94b-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="ff94b-130">L’exemple montre comment utiliser le message [**to \_ GETMAXSIZE**](tb-getmaxsize.md) pour déterminer la taille de tous les éléments de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="ff94b-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="ff94b-131">L’exemple place ensuite la largeur de tous les éléments dans le membre **iWidth** de la structure [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) qui est passée à la notification.</span><span class="sxs-lookup"><span data-stu-id="ff94b-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a><span data-ttu-id="ff94b-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff94b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff94b-133">Utilisation des contrôles de pagineur</span><span class="sxs-lookup"><span data-stu-id="ff94b-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="ff94b-134">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ff94b-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 