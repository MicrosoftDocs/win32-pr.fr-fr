---
title: Création d’une fenêtre
description: Création d’une fenêtre
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea5ec39187b389405d3c6d8eca475944278a3d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103967"
---
# <a name="creating-a-window"></a><span data-ttu-id="3b740-103">Création d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="3b740-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="3b740-104">classes de fenêtre</span><span class="sxs-lookup"><span data-stu-id="3b740-104">Window Classes</span></span>

<span data-ttu-id="3b740-105">Une *classe de fenêtre* définit un ensemble de comportements que plusieurs fenêtres peuvent avoir en commun.</span><span class="sxs-lookup"><span data-stu-id="3b740-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="3b740-106">Par exemple, dans un groupe de boutons, chaque bouton a un comportement similaire quand l’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="3b740-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="3b740-107">Bien entendu, les boutons ne sont pas complètement identiques ; chaque bouton affiche sa propre chaîne de texte et possède ses propres coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="3b740-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="3b740-108">Les données uniques pour chaque fenêtre sont appelées *données d’instance*.</span><span class="sxs-lookup"><span data-stu-id="3b740-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="3b740-109">Chaque fenêtre doit être associée à une classe de fenêtre, même si votre programme ne crée jamais qu’une seule instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3b740-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="3b740-110">Il est important de comprendre qu’une classe de fenêtre n’est pas une « classe » dans le sens C++.</span><span class="sxs-lookup"><span data-stu-id="3b740-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="3b740-111">Au lieu de cela, il s’agit d’une structure de données utilisée en interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3b740-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="3b740-112">Les classes de fenêtre sont inscrites auprès du système au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3b740-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="3b740-113">Pour inscrire une nouvelle classe de fenêtre, commencez par remplir une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) :</span><span class="sxs-lookup"><span data-stu-id="3b740-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="3b740-114">Vous devez définir les membres de structure suivants :</span><span class="sxs-lookup"><span data-stu-id="3b740-114">You must set the following structure members:</span></span>

- <span data-ttu-id="3b740-115">**lpfnWndProc** est un pointeur vers une fonction définie par l’application appelée *procédure de fenêtre* ou « procédure de fenêtre ».</span><span class="sxs-lookup"><span data-stu-id="3b740-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="3b740-116">La procédure de fenêtre définit la plus grande partie du comportement de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="3b740-117">Nous examinerons plus en détail la procédure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="3b740-118">Pour le moment, traitez simplement cela comme une référence anticipée.</span><span class="sxs-lookup"><span data-stu-id="3b740-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="3b740-119">**HINSTANCE** est le handle de l’instance de l’application.</span><span class="sxs-lookup"><span data-stu-id="3b740-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="3b740-120">Obtient cette valeur à partir du paramètre *HINSTANCE* de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="3b740-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="3b740-121">**lpszClassName** est une chaîne qui identifie la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="3b740-122">Comme les noms de classe sont locaux pour le processus actuel, le nom doit être unique au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="3b740-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="3b740-123">Toutefois, les contrôles Windows standard ont également des classes.</span><span class="sxs-lookup"><span data-stu-id="3b740-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="3b740-124">Si vous utilisez l’un de ces contrôles, vous devez choisir des noms de classe qui ne sont pas en conflit avec les noms de classe de contrôle.</span><span class="sxs-lookup"><span data-stu-id="3b740-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="3b740-125">Par exemple, la classe de fenêtre pour le contrôle Button est nommée « Button ».</span><span class="sxs-lookup"><span data-stu-id="3b740-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="3b740-126">La structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) a d’autres membres qui ne sont pas indiqués ici.</span><span class="sxs-lookup"><span data-stu-id="3b740-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="3b740-127">Vous pouvez les définir sur zéro, comme indiqué dans cet exemple, ou les remplir.</span><span class="sxs-lookup"><span data-stu-id="3b740-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="3b740-128">La documentation MSDN décrit en détail la structure.</span><span class="sxs-lookup"><span data-stu-id="3b740-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="3b740-129">Ensuite, transmettez l’adresse de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) à la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="3b740-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="3b740-130">Cette fonction enregistre la classe de fenêtre avec le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3b740-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="3b740-131">Création de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="3b740-131">Creating the Window</span></span>

<span data-ttu-id="3b740-132">Pour créer une nouvelle instance d’une fenêtre, appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) :</span><span class="sxs-lookup"><span data-stu-id="3b740-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

<span data-ttu-id="3b740-133">Vous pouvez consulter les descriptions des paramètres détaillés sur MSDN, mais voici un récapitulatif rapide :</span><span class="sxs-lookup"><span data-stu-id="3b740-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="3b740-134">Le premier paramètre vous permet de spécifier des comportements facultatifs pour la fenêtre (par exemple, des fenêtres transparentes).</span><span class="sxs-lookup"><span data-stu-id="3b740-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="3b740-135">Définissez ce paramètre sur zéro pour les comportements par défaut.</span><span class="sxs-lookup"><span data-stu-id="3b740-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="3b740-136">`CLASS_NAME` nom de la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="3b740-137">Définit le type de fenêtre que vous êtes en train de créer.</span><span class="sxs-lookup"><span data-stu-id="3b740-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="3b740-138">Le texte de la fenêtre est utilisé de différentes façons par différents types de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="3b740-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="3b740-139">Si la fenêtre a une barre de titre, le texte est affiché dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="3b740-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="3b740-140">Le style de fenêtre est un ensemble d’indicateurs qui définissent l’apparence et la convivialité d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="3b740-141">En fait, la constante **WS \_ OVERLAPPEDWINDOW** est associée à plusieurs indicateurs avec une **opération or au** niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="3b740-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="3b740-142">Ensemble, ces indicateurs donnent à la fenêtre une barre de titre, une bordure, un menu système et des boutons **réduire** et **agrandir** .</span><span class="sxs-lookup"><span data-stu-id="3b740-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="3b740-143">Cet ensemble d’indicateurs est le style le plus courant pour une fenêtre d’application de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="3b740-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="3b740-144">Pour la position et la taille, la constante **CW \_ usedefault** signifie utiliser les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="3b740-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="3b740-145">Le paramètre suivant définit une fenêtre parente ou une fenêtre propriétaire pour la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="3b740-146">Définissez le parent si vous créez une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="3b740-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="3b740-147">Pour une fenêtre de niveau supérieur, affectez-lui la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="3b740-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="3b740-148">Pour une fenêtre d’application, le paramètre suivant définit le menu de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="3b740-149">Cet exemple n’utilise pas de menu, donc la valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="3b740-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="3b740-150">*HINSTANCE* est le descripteur d’instance, décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="3b740-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="3b740-151">(Consultez [WinMain : le point d’entrée de l’application](winmain--the-application-entry-point.md).)</span><span class="sxs-lookup"><span data-stu-id="3b740-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="3b740-152">Le dernier paramètre est un pointeur vers des données arbitraires de type **void \***.</span><span class="sxs-lookup"><span data-stu-id="3b740-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="3b740-153">Vous pouvez utiliser cette valeur pour passer une structure de données à votre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="3b740-154">Nous allons vous montrer une manière possible d’utiliser ce paramètre dans la section gestion de l’état de l' [application](managing-application-state-.md).</span><span class="sxs-lookup"><span data-stu-id="3b740-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="3b740-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) retourne un handle vers la nouvelle fenêtre, ou zéro si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="3b740-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="3b740-156">Pour afficher la fenêtre, c’est-à-dire rendre la fenêtre visible, transmettez le handle de fenêtre à la fonction [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) :</span><span class="sxs-lookup"><span data-stu-id="3b740-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="3b740-157">Le paramètre *HWND* est le handle de fenêtre retourné par [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="3b740-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="3b740-158">Le paramètre *nCmdShow* peut être utilisé pour réduire ou agrandir une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="3b740-159">Le système d’exploitation transmet cette valeur au programme par le biais de la fonction **wWinMain** .</span><span class="sxs-lookup"><span data-stu-id="3b740-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="3b740-160">Voici le code complet pour créer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b740-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="3b740-161">N’oubliez pas que `WindowProc` n’est toujours qu’une déclaration anticipée d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="3b740-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="3b740-162">Félicitations, vous avez créé une fenêtre !</span><span class="sxs-lookup"><span data-stu-id="3b740-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="3b740-163">Pour le moment, la fenêtre ne contient pas de contenu ou n’interagit pas avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3b740-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="3b740-164">Dans une application GUI réelle, la fenêtre répond aux événements de l’utilisateur et du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3b740-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="3b740-165">La section suivante décrit comment les messages de fenêtre fournissent ce type d’interactivité.</span><span class="sxs-lookup"><span data-stu-id="3b740-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="3b740-166">Suivant</span><span class="sxs-lookup"><span data-stu-id="3b740-166">Next</span></span>

[<span data-ttu-id="3b740-167">Messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="3b740-167">Window Messages</span></span>](window-messages.md)
