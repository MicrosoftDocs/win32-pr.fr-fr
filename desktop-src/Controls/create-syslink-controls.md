---
title: Comment créer des contrôles SysLink
description: Implémentez les liens hypertexte du contrôle SysLink par le biais du balisage dans la chaîne d’initialisation du contrôle, ou en lui envoyant un \_ message LM SETITEM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730653"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="c70d4-103">Comment créer des contrôles SysLink</span><span class="sxs-lookup"><span data-stu-id="c70d4-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="c70d4-104">Implémentez les liens hypertexte du contrôle SysLink par le biais du balisage dans la chaîne d’initialisation du contrôle, ou en lui envoyant un message [**LM \_ SETITEM**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c70d4-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="c70d4-105">Avant de créer des contrôles SysLink, vous devez appeler la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant la \_ classe de liaison ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="c70d4-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="c70d4-106">Pour créer un SysLink, appelez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de [**\_ liaison WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="c70d4-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="c70d4-107">Le paramètre *lpWindowName* qui est commun à ces fonctions spécifie un pointeur vers une chaîne se terminant par zéro qui contient le texte marqué à afficher.</span><span class="sxs-lookup"><span data-stu-id="c70d4-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="c70d4-108">Pour les styles de fenêtre particuliers aux contrôles SysLink, consultez [Syslink Control styles](syslink-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="c70d4-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c70d4-109">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c70d4-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c70d4-110">Technologies</span><span class="sxs-lookup"><span data-stu-id="c70d4-110">Technologies</span></span>

-   [<span data-ttu-id="c70d4-111">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="c70d4-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c70d4-112">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c70d4-112">Prerequisites</span></span>

-   <span data-ttu-id="c70d4-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="c70d4-113">C/C++</span></span>
-   <span data-ttu-id="c70d4-114">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="c70d4-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c70d4-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="c70d4-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="c70d4-116">Créer un contrôle SysLink</span><span class="sxs-lookup"><span data-stu-id="c70d4-116">Create a SysLink Control</span></span>

<span data-ttu-id="c70d4-117">L’exemple de code suivant crée un contrôle SysLink qui affiche deux liens hypertexte.</span><span class="sxs-lookup"><span data-stu-id="c70d4-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="c70d4-118">Le premier lien hypertexte est une URL Internet et le second est défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="c70d4-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="c70d4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c70d4-119">Remarks</span></span>

<span data-ttu-id="c70d4-120">Il est supposé que [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) a déjà été appelé.</span><span class="sxs-lookup"><span data-stu-id="c70d4-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="c70d4-121">Si vous spécifiez le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) , l’utilisateur est en mesure de sélectionner un lien en cliquant dessus et en appuyant sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="c70d4-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="c70d4-122">La version 6 de ComCtl32.dll prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="c70d4-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="c70d4-123">Par conséquent, vous ne pouvez pas créer de versions ANSI de contrôles SysLink (Unicode uniquement).</span><span class="sxs-lookup"><span data-stu-id="c70d4-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c70d4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c70d4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c70d4-125">Utilisation des contrôles SysLink</span><span class="sxs-lookup"><span data-stu-id="c70d4-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="c70d4-126">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c70d4-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 