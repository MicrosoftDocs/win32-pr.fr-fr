---
title: Contrôles de sous-classe
description: Si un contrôle effectue presque tout ce que vous souhaitez, mais que vous avez besoin de quelques fonctionnalités supplémentaires, vous pouvez modifier ou ajouter des fonctionnalités au contrôle d’origine en le sous-classant.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031956"
---
# <a name="subclassing-controls"></a><span data-ttu-id="5314d-103">Contrôles de sous-classe</span><span class="sxs-lookup"><span data-stu-id="5314d-103">Subclassing Controls</span></span>

<span data-ttu-id="5314d-104">Si un contrôle effectue presque tout ce que vous souhaitez, mais que vous avez besoin de quelques fonctionnalités supplémentaires, vous pouvez modifier ou ajouter des fonctionnalités au contrôle d’origine en le sous-classant.</span><span class="sxs-lookup"><span data-stu-id="5314d-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="5314d-105">Une sous-classe peut avoir toutes les fonctionnalités d’une classe existante, ainsi que toutes les fonctionnalités supplémentaires que vous souhaitez lui attribuer.</span><span class="sxs-lookup"><span data-stu-id="5314d-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="5314d-106">Ce document explique comment créer des sous-classes et comprend les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="5314d-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="5314d-107">Sous-classement des contrôles avant ComCtl32.dll version 6</span><span class="sxs-lookup"><span data-stu-id="5314d-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="5314d-108">Stockage des données utilisateur</span><span class="sxs-lookup"><span data-stu-id="5314d-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="5314d-109">Inconvénients de l’ancienne approche de sous-classe</span><span class="sxs-lookup"><span data-stu-id="5314d-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="5314d-110">Sous-classer des contrôles à l’aide de ComCtl32.dll version 6</span><span class="sxs-lookup"><span data-stu-id="5314d-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="5314d-111">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="5314d-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="5314d-112">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="5314d-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="5314d-113">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="5314d-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="5314d-114">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="5314d-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="5314d-115">Sous-classement des contrôles avant ComCtl32.dll version 6</span><span class="sxs-lookup"><span data-stu-id="5314d-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="5314d-116">Vous pouvez placer un contrôle dans une sous-classe et stocker des données utilisateur dans un contrôle.</span><span class="sxs-lookup"><span data-stu-id="5314d-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="5314d-117">Vous effectuez cette opération lorsque vous utilisez des versions de ComCtl32.dll antérieures à la version 6.</span><span class="sxs-lookup"><span data-stu-id="5314d-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="5314d-118">La création de sous-classes avec des versions antérieures de ComCtl32.dll présente quelques inconvénients.</span><span class="sxs-lookup"><span data-stu-id="5314d-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="5314d-119">Pour créer un nouveau contrôle, il est préférable de commencer par l’un des contrôles communs Windows et de l’étendre pour répondre à un besoin particulier.</span><span class="sxs-lookup"><span data-stu-id="5314d-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="5314d-120">Pour étendre un contrôle, créez un contrôle et remplacez sa procédure de fenêtre existante par un nouveau.</span><span class="sxs-lookup"><span data-stu-id="5314d-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="5314d-121">La nouvelle procédure intercepte les messages du contrôle et les agit ou les transmet à la procédure d’origine pour le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="5314d-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="5314d-122">Utilisez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ou [**SETWINDOWLONGPTR**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) pour remplacer WNDPROC du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5314d-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="5314d-123">L’exemple de code suivant montre comment remplacer un WNDPROC.</span><span class="sxs-lookup"><span data-stu-id="5314d-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="5314d-124">Stockage des données utilisateur</span><span class="sxs-lookup"><span data-stu-id="5314d-124">Storing User Data</span></span>

<span data-ttu-id="5314d-125">Vous souhaiterez peut-être stocker les données utilisateur avec une fenêtre individuelle.</span><span class="sxs-lookup"><span data-stu-id="5314d-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="5314d-126">Ces données peuvent être utilisées par la nouvelle procédure de fenêtre pour déterminer comment dessiner le contrôle ou où envoyer certains messages.</span><span class="sxs-lookup"><span data-stu-id="5314d-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="5314d-127">Par exemple, vous pouvez utiliser des données pour stocker un pointeur de classe C++ vers la classe qui représente le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5314d-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="5314d-128">L’exemple de code suivant montre comment utiliser [**échec SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) pour stocker des données avec une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5314d-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="5314d-129">Inconvénients de l’ancienne approche de sous-classe</span><span class="sxs-lookup"><span data-stu-id="5314d-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="5314d-130">La liste suivante décrit certains des inconvénients liés à l’utilisation de l’approche décrite précédemment pour la sous-classement d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="5314d-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="5314d-131">La procédure de fenêtre ne peut être remplacée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="5314d-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="5314d-132">Il est difficile de supprimer une sous-classe après sa création.</span><span class="sxs-lookup"><span data-stu-id="5314d-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="5314d-133">L’Association de données privées à une fenêtre est inefficace.</span><span class="sxs-lookup"><span data-stu-id="5314d-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="5314d-134">Pour appeler la procédure suivante dans une chaîne de sous-classes, vous ne pouvez pas effectuer un cast de l’ancienne procédure de fenêtre et l’appeler, vous devez l’appeler à l’aide de la fonction [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="5314d-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="5314d-135">Sous-classer des contrôles à l’aide de ComCtl32.dll version 6</span><span class="sxs-lookup"><span data-stu-id="5314d-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="5314d-136">ComCtl32.dll version 6 est Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="5314d-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="5314d-137">Les contrôles communs pris en charge par ComCtl32.dll version 6 ne doivent pas être sous-classés (ou superclassés) avec des procédures de fenêtre ANSI.</span><span class="sxs-lookup"><span data-stu-id="5314d-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="5314d-138">ComCtl32.dll version 6 contient quatre fonctions qui facilitent la création de sous-classes et éliminent les inconvénients évoqués précédemment.</span><span class="sxs-lookup"><span data-stu-id="5314d-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="5314d-139">Les nouvelles fonctions encapsulent la gestion impliquée dans plusieurs jeux de données de référence. par conséquent, le développeur peut se concentrer sur les fonctionnalités de programmation et non sur la gestion des sous-classes.</span><span class="sxs-lookup"><span data-stu-id="5314d-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="5314d-140">Les fonctions de sous-classe sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5314d-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="5314d-141">**SetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="5314d-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="5314d-142">**GetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="5314d-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="5314d-143">**RemoveWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="5314d-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="5314d-144">**DefSubclassProc**</span><span class="sxs-lookup"><span data-stu-id="5314d-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="5314d-145">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="5314d-145">SetWindowSubclass</span></span>

<span data-ttu-id="5314d-146">Cette fonction est utilisée pour initialiser la sous-classe d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5314d-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="5314d-147">Chaque sous-classe est identifiée de manière unique par l’adresse du *pfnSubclass* et de son *uIdSubclass*.</span><span class="sxs-lookup"><span data-stu-id="5314d-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="5314d-148">Il s’agit des paramètres de la fonction [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) .</span><span class="sxs-lookup"><span data-stu-id="5314d-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="5314d-149">Plusieurs sous-classes peuvent partager la même procédure de sous-classe et l’ID peut identifier chaque appel.</span><span class="sxs-lookup"><span data-stu-id="5314d-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="5314d-150">Pour modifier des données de référence, vous pouvez effectuer des appels ultérieurs à **SetWindowSubclass**.</span><span class="sxs-lookup"><span data-stu-id="5314d-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="5314d-151">L’avantage principal est que chaque instance de sous-classe possède ses propres données de référence.</span><span class="sxs-lookup"><span data-stu-id="5314d-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="5314d-152">La déclaration d’une procédure de sous-classe est légèrement différente de celle d’une procédure de fenêtre normale, car elle contient deux éléments de données supplémentaires : l’ID de sous-classe et les données de référence.</span><span class="sxs-lookup"><span data-stu-id="5314d-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="5314d-153">Les deux derniers paramètres de la déclaration de fonction suivante illustrent cela.</span><span class="sxs-lookup"><span data-stu-id="5314d-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="5314d-154">Chaque fois qu’un message est reçu par la nouvelle procédure de fenêtre, un ID de sous-classe et des données de référence sont inclus.</span><span class="sxs-lookup"><span data-stu-id="5314d-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="5314d-155">Toutes les chaînes passées à la procédure sont des chaînes Unicode même si Unicode n’est pas spécifié en tant que définition de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="5314d-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="5314d-156">L’exemple suivant montre une implémentation squelette d’une procédure de fenêtre pour un contrôle sous-classé.</span><span class="sxs-lookup"><span data-stu-id="5314d-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="5314d-157">La procédure de fenêtre peut être attachée au contrôle dans le gestionnaire [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) de la procédure de dialogue, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5314d-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="5314d-158">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="5314d-158">GetWindowSubclass</span></span>

<span data-ttu-id="5314d-159">Cette fonction récupère des informations sur une sous-classe.</span><span class="sxs-lookup"><span data-stu-id="5314d-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="5314d-160">Par exemple, vous pouvez utiliser [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) pour accéder aux données de référence.</span><span class="sxs-lookup"><span data-stu-id="5314d-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="5314d-161">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="5314d-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="5314d-162">Cette fonction supprime les sous-classes.</span><span class="sxs-lookup"><span data-stu-id="5314d-162">This function removes subclasses.</span></span> <span data-ttu-id="5314d-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) en association avec [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) vous permet d’ajouter et de supprimer dynamiquement des sous-classes.</span><span class="sxs-lookup"><span data-stu-id="5314d-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="5314d-164">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="5314d-164">DefSubclassProc</span></span>

<span data-ttu-id="5314d-165">La fonction [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) appelle le gestionnaire suivant dans la chaîne de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="5314d-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="5314d-166">La fonction récupère également l’ID et les données de référence appropriés et transmet les informations à la procédure de fenêtre suivante.</span><span class="sxs-lookup"><span data-stu-id="5314d-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 