---
title: Écriture de la procédure de fenêtre
description: Écriture de la procédure de fenêtre
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105717"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="f4bbb-103">Écriture de la procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="f4bbb-103">Writing the Window Procedure</span></span>

<span data-ttu-id="f4bbb-104">La fonction [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) appelle la procédure de fenêtre de la fenêtre qui est la cible du message.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="f4bbb-105">La procédure de fenêtre a la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="f4bbb-106">Il y a quatre paramètres :</span><span class="sxs-lookup"><span data-stu-id="f4bbb-106">There are four parameters:</span></span>

- <span data-ttu-id="f4bbb-107">*HWND* est un handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="f4bbb-108">*uMsg* est le code du message ; par exemple, le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) indique que la fenêtre a été redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="f4bbb-109">*wParam* et *lParam* contiennent des données supplémentaires relatives au message.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="f4bbb-110">La signification exacte dépend du code du message.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="f4bbb-111">**LRESULT** est une valeur entière que votre programme retourne à Windows.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="f4bbb-112">Elle contient la réponse de votre programme à un message particulier.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="f4bbb-113">La signification de cette valeur dépend du code du message.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="f4bbb-114">Le **rappel** est la Convention d’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="f4bbb-115">Une procédure de fenêtre classique est simplement une grande instruction switch qui bascule sur le code du message.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="f4bbb-116">Ajoutez des cas pour chaque message que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="f4bbb-117">Les données supplémentaires du message sont contenues dans les paramètres *lParam* et *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f4bbb-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="f4bbb-118">Les deux paramètres sont des valeurs entières de la taille d’une largeur de pointeur (32 bits ou 64 bits).</span><span class="sxs-lookup"><span data-stu-id="f4bbb-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="f4bbb-119">La signification de chaque dépend du code du message (*uMsg*).</span><span class="sxs-lookup"><span data-stu-id="f4bbb-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="f4bbb-120">Pour chaque message, vous devrez rechercher le code du message sur MSDN et effectuer un cast des paramètres vers le type de données correct.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="f4bbb-121">En général, les données sont soit une valeur numérique, soit un pointeur vers une structure.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="f4bbb-122">Certains messages n’ont pas de données.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-122">Some messages do not have any data.</span></span>

<span data-ttu-id="f4bbb-123">Par exemple, la documentation du message [**de \_ taille WM**](/windows/desktop/winmsg/wm-size) indique que :</span><span class="sxs-lookup"><span data-stu-id="f4bbb-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="f4bbb-124">*wParam* est un indicateur qui indique si la fenêtre a été réduite, agrandie ou redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="f4bbb-125">*lParam* contient les nouvelles largeur et hauteur de la fenêtre sous forme de valeurs 16 bits compressées en nombre de 1 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="f4bbb-126">Vous devrez effectuer des décalages de bits pour récupérer ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="f4bbb-127">Heureusement, le fichier d’en-tête WinDef. h contient des macros d’assistance qui le font.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="f4bbb-128">Une procédure de fenêtre classique gère des dizaines de messages, donc elle peut croître très longtemps.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="f4bbb-129">Une façon de rendre votre code plus modulaire consiste à placer la logique nécessaire pour gérer chaque message dans une fonction distincte.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="f4bbb-130">Dans la procédure de fenêtre, effectuez un cast des paramètres *wParam* et *lParam* vers le type de données correct, puis transmettez ces valeurs à la fonction.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="f4bbb-131">Par exemple, pour gérer le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) , la procédure de fenêtre ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="f4bbb-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

<span data-ttu-id="f4bbb-132">Les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) récupèrent les valeurs de largeur et de hauteur de 16 bits à partir de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="f4bbb-133">(Vous pouvez rechercher ces types de détails dans la documentation MSDN pour chaque code de message). La procédure de fenêtre extrait la largeur et la hauteur, puis passe ces valeurs à la `OnSize` fonction.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="f4bbb-134">Gestion des messages par défaut</span><span class="sxs-lookup"><span data-stu-id="f4bbb-134">Default Message Handling</span></span>

<span data-ttu-id="f4bbb-135">Si vous ne gérez pas un message particulier dans votre procédure de fenêtre, transmettez les paramètres de message directement à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="f4bbb-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="f4bbb-136">Cette fonction effectue l’action par défaut pour le message, qui varie selon le type de message.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="f4bbb-137">Éviter les goulots d’étranglement dans votre procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="f4bbb-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="f4bbb-138">Pendant que votre procédure de fenêtre s’exécute, elle bloque tous les autres messages pour les fenêtres créées sur le même thread.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="f4bbb-139">Par conséquent, évitez un traitement long à l’intérieur de votre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="f4bbb-140">Par exemple, supposons que votre programme ouvre une connexion TCP et attend indéfiniment que le serveur réponde.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="f4bbb-141">Si vous le faites à l’intérieur de la procédure de fenêtre, votre interface utilisateur ne répondra pas tant que la demande n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="f4bbb-142">Pendant ce temps, la fenêtre ne peut pas traiter l’entrée de la souris ou du clavier, se redessiner ou même se fermer.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="f4bbb-143">Au lieu de cela, vous devez déplacer le travail vers un autre thread, à l’aide de l’une des fonctionnalités multitâche intégrées à Windows :</span><span class="sxs-lookup"><span data-stu-id="f4bbb-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="f4bbb-144">Créez un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-144">Create a new thread.</span></span>
- <span data-ttu-id="f4bbb-145">Utiliser un pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-145">Use a thread pool.</span></span>
- <span data-ttu-id="f4bbb-146">Utilisez des appels d’e/s asynchrones.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="f4bbb-147">Utilisez des appels de procédure asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f4bbb-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="f4bbb-148">Suivant</span><span class="sxs-lookup"><span data-stu-id="f4bbb-148">Next</span></span>

[<span data-ttu-id="f4bbb-149">Peindre la fenêtre</span><span class="sxs-lookup"><span data-stu-id="f4bbb-149">Painting the Window</span></span>](painting-the-window.md)
