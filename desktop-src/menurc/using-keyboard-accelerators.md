---
title: Utilisation des accélérateurs clavier
description: Cette section traite des tâches associées aux accélérateurs de clavier.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- entrée d’utilisateur, accélérateurs de clavier
- capture de l’entrée utilisateur, accélérateurs de clavier
- accélérateurs de clavier
- accélérateurs
- tables d’accélérateurs
- ressources de table d’accélérateurs
- fonction d’accélérateur translate
- Message WM_COMMAND
- WM_SYS message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031227"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="66769-112">Utilisation des accélérateurs clavier</span><span class="sxs-lookup"><span data-stu-id="66769-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="66769-113">Cette section traite des tâches associées aux accélérateurs de clavier.</span><span class="sxs-lookup"><span data-stu-id="66769-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="66769-114">Utilisation d’une ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="66769-115">Création de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="66769-116">Chargement de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="66769-117">Appel de la fonction d’accélérateur translate</span><span class="sxs-lookup"><span data-stu-id="66769-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="66769-118">Traitement des \_ messages de commande WM</span><span class="sxs-lookup"><span data-stu-id="66769-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="66769-119">Destruction de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="66769-120">Création d’accélérateurs pour les attributs de police</span><span class="sxs-lookup"><span data-stu-id="66769-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="66769-121">Utilisation d’une table d’accélérateurs créée au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="66769-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="66769-122">Création d’une table d’accélérateurs Run-Time</span><span class="sxs-lookup"><span data-stu-id="66769-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="66769-123">Accélérateurs de traitement</span><span class="sxs-lookup"><span data-stu-id="66769-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="66769-124">Destruction d’une table d’accélérateurs de Run-Time</span><span class="sxs-lookup"><span data-stu-id="66769-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="66769-125">Création d’accélérateurs modifiables par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="66769-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="66769-126">Utilisation d’une ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="66769-127">La méthode la plus courante pour ajouter la prise en charge des accélérateurs à une application consiste à inclure une ressource de table d’accélérateurs avec le fichier exécutable de l’application, puis à charger la ressource au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="66769-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="66769-128">Cette section couvre les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="66769-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="66769-129">Création de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="66769-130">Chargement de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="66769-131">Appel de la fonction d’accélérateur translate</span><span class="sxs-lookup"><span data-stu-id="66769-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="66769-132">Traitement des \_ messages de commande WM</span><span class="sxs-lookup"><span data-stu-id="66769-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="66769-133">Destruction de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="66769-134">Création d’accélérateurs pour les attributs de police</span><span class="sxs-lookup"><span data-stu-id="66769-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="66769-135">Création de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="66769-136">Vous créez une ressource de table d’accélérateurs à l’aide de [l’instruction Accelerators dans le fichier](./accelerators-resource.md) de définition de ressource de votre application.</span><span class="sxs-lookup"><span data-stu-id="66769-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="66769-137">Vous devez affecter un nom ou un identificateur de ressource à la table d’accélérateurs, de préférence à la différence de toute autre ressource.</span><span class="sxs-lookup"><span data-stu-id="66769-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="66769-138">Le système utilise cet identificateur pour charger la ressource au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="66769-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="66769-139">Chaque accélérateur que vous définissez requiert une entrée distincte dans la table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="66769-140">Dans chaque entrée, vous définissez la séquence de touches (un code de caractère ASCII ou un code de clé virtuelle) qui génère l’accélérateur et l’identificateur de l’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="66769-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="66769-141">Vous devez également spécifier si la séquence de touches doit être utilisée dans une combinaison avec les touches ALT, Maj ou CTRL.</span><span class="sxs-lookup"><span data-stu-id="66769-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="66769-142">Pour plus d’informations sur les clés virtuelles, consultez [entrée au clavier](/windows/desktop/inputdev/keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="66769-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="66769-143">Une séquence de touches ASCII est spécifiée en plaçant le caractère ASCII entre des guillemets doubles ou en utilisant la valeur entière du caractère en combinaison avec l’indicateur ASCII.</span><span class="sxs-lookup"><span data-stu-id="66769-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="66769-144">Les exemples suivants montrent comment définir des accélérateurs ASCII.</span><span class="sxs-lookup"><span data-stu-id="66769-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="66769-145">Une séquence de touches de code de touche virtuelle est spécifiée différemment selon que la séquence de touches est une clé alphanumérique ou une clé non alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="66769-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="66769-146">Pour une clé alphanumérique, la lettre ou le chiffre de la clé, placé entre guillemets doubles, est combiné avec l’indicateur **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="66769-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="66769-147">Pour une clé non alphanumérique, le code de la clé virtuelle pour la clé spécifique est combiné avec l’indicateur **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="66769-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="66769-148">Les exemples suivants montrent comment définir des accélérateurs de code de clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66769-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="66769-149">L’exemple suivant montre une ressource de table d’accélérateurs qui définit des accélérateurs pour les opérations de fichier.</span><span class="sxs-lookup"><span data-stu-id="66769-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="66769-150">Le nom de la ressource est *FileAccel*.</span><span class="sxs-lookup"><span data-stu-id="66769-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="66769-151">Si vous souhaitez que l’utilisateur appuie sur les touches ALT, Maj ou CTRL dans une combinaison avec la touche d’accès rapide, spécifiez les indicateurs ALT, Maj et contrôle dans la définition de l’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="66769-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="66769-152">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="66769-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="66769-153">Par défaut, lorsqu’une touche d’accès rapide correspond à un élément de menu, le système met en surbrillance l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="66769-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="66769-154">Vous pouvez utiliser l’indicateur **noinverse** pour empêcher la mise en surbrillance d’un accélérateur individuel.</span><span class="sxs-lookup"><span data-stu-id="66769-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="66769-155">L’exemple suivant montre comment utiliser l’indicateur **noinverse** :</span><span class="sxs-lookup"><span data-stu-id="66769-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="66769-156">Pour définir des accélérateurs qui correspondent à des éléments de menu dans votre application, incluez les accélérateurs dans le texte des éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="66769-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="66769-157">L’exemple suivant montre comment inclure des accélérateurs dans un texte d’élément de menu dans un fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="66769-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="66769-158">Chargement de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="66769-159">Une application charge une ressource de table d’accélérateurs en appelant la fonction [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) et en spécifiant le handle d’instance pour l’application dont le fichier exécutable contient la ressource, ainsi que le nom ou l’identificateur de la ressource.</span><span class="sxs-lookup"><span data-stu-id="66769-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="66769-160">**LoadAccelerators** charge la table d’accélérateurs spécifiée en mémoire et retourne le handle de la table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="66769-161">Une application peut charger une ressource de table d’accélérateurs à tout moment.</span><span class="sxs-lookup"><span data-stu-id="66769-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="66769-162">En règle générale, une application à thread unique charge sa table d’accélérateurs avant d’entrer dans sa boucle de message principale.</span><span class="sxs-lookup"><span data-stu-id="66769-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="66769-163">Une application qui utilise plusieurs threads charge généralement la ressource de table d’accélérateurs pour un thread avant d’entrer dans la boucle de message pour le thread.</span><span class="sxs-lookup"><span data-stu-id="66769-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="66769-164">Une application ou un thread peut également utiliser plusieurs tables d’accélérateurs, chacune associée à une fenêtre particulière dans l’application.</span><span class="sxs-lookup"><span data-stu-id="66769-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="66769-165">Une telle application chargera la table d’accélérateurs pour la fenêtre chaque fois que l’utilisateur activera la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66769-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="66769-166">Pour plus d’informations sur les threads, consultez [processus et threads](/windows/desktop/ProcThread/processes-and-threads).</span><span class="sxs-lookup"><span data-stu-id="66769-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="66769-167">Appel de la fonction d’accélérateur translate</span><span class="sxs-lookup"><span data-stu-id="66769-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="66769-168">Pour traiter les accélérateurs, la boucle de message d’une application (ou du thread) doit contenir un appel à la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) .</span><span class="sxs-lookup"><span data-stu-id="66769-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="66769-169">**TranslateAccelerator** compare les séquences de touches à une table d’accélérateurs et, s’il trouve une correspondance, traduit les séquences de touches en un message de [**\_ commande WM**](wm-command.md) (ou [**WM \_ SYSCOMMAND**](wm-syscommand.md)).</span><span class="sxs-lookup"><span data-stu-id="66769-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="66769-170">La fonction envoie ensuite le message à une procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66769-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="66769-171">Les paramètres de la fonction **TranslateAccelerator** incluent le descripteur de la fenêtre qui doit recevoir les messages de **\_ commande WM** , le handle vers la table d’accélérateurs utilisée pour convertir les accélérateurs et un pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) contenant un message de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="66769-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="66769-172">L’exemple suivant montre comment appeler **TranslateAccelerator** à partir d’une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="66769-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="66769-173">Traitement des \_ messages de commande WM</span><span class="sxs-lookup"><span data-stu-id="66769-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="66769-174">Quand un accélérateur est utilisé, la fenêtre spécifiée dans la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) reçoit une [**\_ commande WM**](wm-command.md) ou un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="66769-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="66769-175">Le mot de poids faible du paramètre *wParam* contient l’identificateur de l’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="66769-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="66769-176">La procédure de fenêtre examine l’identificateur pour déterminer la source du message de **\_ commande WM** et traiter le message en conséquence.</span><span class="sxs-lookup"><span data-stu-id="66769-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="66769-177">En règle générale, si un accélérateur correspond à un élément de menu dans l’application, l’accélérateur et l’élément de menu se voient attribuer le même identificateur.</span><span class="sxs-lookup"><span data-stu-id="66769-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="66769-178">Si vous avez besoin de savoir si un message de [**\_ commande WM**](wm-command.md) a été généré par un accélérateur ou par un élément de menu, vous pouvez examiner le mot de poids fort du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="66769-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="66769-179">Si un accélérateur a généré le message, le mot de poids fort est 1 ; Si un élément de menu a généré le message, le mot de poids fort est 0.</span><span class="sxs-lookup"><span data-stu-id="66769-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="66769-180">Destruction de la ressource de table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="66769-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="66769-181">Le système détruit automatiquement les ressources de table d’accélérateurs chargées par la fonction [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , en supprimant la ressource de la mémoire après la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="66769-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="66769-182">Création d’accélérateurs pour les attributs de police</span><span class="sxs-lookup"><span data-stu-id="66769-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="66769-183">L’exemple de cette section montre comment effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="66769-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="66769-184">Créez une ressource de table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="66769-185">Chargez la table d’accélérateurs au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="66769-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="66769-186">Traduisez des accélérateurs dans une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="66769-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="66769-187">Traitez les messages de [**\_ commande WM**](wm-command.md) générés par les accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="66769-188">Ces tâches sont démontrées dans le contexte d’une application qui comprend un menu de **caractères** et des accélérateurs correspondants qui permettent à l’utilisateur de sélectionner les attributs de la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="66769-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="66769-189">La partie suivante d’un fichier de définition de ressource définit le menu **caractère** et la table d’accélérateurs associée.</span><span class="sxs-lookup"><span data-stu-id="66769-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="66769-190">Notez que les éléments de menu affichent les séquences de touches d’accélérateur et que chaque accélérateur a le même identificateur que son élément de menu associé.</span><span class="sxs-lookup"><span data-stu-id="66769-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="66769-191">Les sections suivantes du fichier source de l’application montrent comment implémenter les accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="66769-192">Utilisation d’une table d’accélérateurs créée au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="66769-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="66769-193">Cette rubrique explique comment utiliser des tables d’accélérateurs créées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="66769-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="66769-194">Création d’une table d’accélérateurs Run-Time</span><span class="sxs-lookup"><span data-stu-id="66769-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="66769-195">Accélérateurs de traitement</span><span class="sxs-lookup"><span data-stu-id="66769-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="66769-196">Destruction d’une table d’accélérateurs de Run-Time</span><span class="sxs-lookup"><span data-stu-id="66769-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="66769-197">Création d’accélérateurs modifiables par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="66769-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="66769-198">Création d’une table d’accélérateurs Run-Time</span><span class="sxs-lookup"><span data-stu-id="66769-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="66769-199">La première étape de la création d’une table d’accélérateurs au moment de l’exécution est le remplissage d’un tableau de structures d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="66769-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="66769-200">Chaque structure du tableau définit un accélérateur dans la table.</span><span class="sxs-lookup"><span data-stu-id="66769-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="66769-201">La définition d’un accélérateur comprend ses indicateurs, sa clé et son identificateur.</span><span class="sxs-lookup"><span data-stu-id="66769-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="66769-202">La structure d' **accélération** se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="66769-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="66769-203">Vous définissez la séquence de touches d’un accélérateur en spécifiant un code de caractère ASCII ou une clé virtuelle dans le membre **clé** de la structure d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="66769-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="66769-204">Si vous spécifiez un code de clé virtuelle, vous devez d’abord inclure l’indicateur **FVIRTKEY** dans le membre **fVirt** ; dans le cas contraire, le système interprète le code comme un code de caractère ASCII.</span><span class="sxs-lookup"><span data-stu-id="66769-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="66769-205">Vous pouvez inclure l’indicateur **FCONTROL**, **Falt** ou **FSHIFT** , ou les trois, pour combiner la touche Ctrl, ALT ou Maj avec la séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="66769-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="66769-206">Pour créer la table d’accélérateurs, transmettez un pointeur vers le tableau de structures d' [**accélération**](/windows/win32/api/winuser/ns-winuser-accel) à la fonction [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) .</span><span class="sxs-lookup"><span data-stu-id="66769-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="66769-207">**CreateAcceleratorTable** crée la table d’accélérateurs et retourne le descripteur à la table.</span><span class="sxs-lookup"><span data-stu-id="66769-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="66769-208">Accélérateurs de traitement</span><span class="sxs-lookup"><span data-stu-id="66769-208">Processing Accelerators</span></span>

<span data-ttu-id="66769-209">Le processus de chargement et d’appel des accélérateurs fournis par une table d’accélérateurs créée au moment de l’exécution est identique au traitement de ceux fournis par une ressource de table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="66769-210">Pour plus d’informations, consultez [chargement de la ressource de table d’accélérateurs via le traitement des](#loading-the-accelerator-table-resource) messages de [ \_ commande WM](/windows).</span><span class="sxs-lookup"><span data-stu-id="66769-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="66769-211">Destruction d’une table d’accélérateurs de Run-Time</span><span class="sxs-lookup"><span data-stu-id="66769-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="66769-212">Le système détruit automatiquement les tables d’accélérateurs créées au moment de l’exécution, en supprimant les ressources de la mémoire après la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="66769-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="66769-213">Vous pouvez détruire une table d’accélérateurs et la supprimer de la mémoire plus tôt en passant le handle de la table à la fonction [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .</span><span class="sxs-lookup"><span data-stu-id="66769-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="66769-214">Création d’accélérateurs modifiables par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="66769-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="66769-215">Cet exemple montre comment construire une boîte de dialogue qui permet à l’utilisateur de modifier l’accélérateur associé à un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="66769-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="66769-216">La boîte de dialogue se compose d’une zone de liste déroulante contenant des éléments de menu, d’une zone de liste déroulante contenant les noms des clés et de cases à cocher permettant de sélectionner les touches CTRL, ALT et Maj.</span><span class="sxs-lookup"><span data-stu-id="66769-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="66769-217">L’illustration suivante montre la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="66769-217">The following illustration shows the dialog box.</span></span>

![boîte de dialogue avec des zones de liste déroulante et des cases à cocher](images/useredit.gif)

<span data-ttu-id="66769-219">L’exemple suivant montre comment la boîte de dialogue est définie dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="66769-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="66769-220">La barre de menus de l’application contient un sous-menu de **caractères** dont les éléments sont associés à des accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="66769-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="66769-221">Les valeurs d’élément de menu du modèle de menu sont des constantes définies comme suit dans le fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="66769-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="66769-222">La boîte de dialogue utilise un tableau de structures VKEY définies par l’application, chacune contenant une chaîne de texte de frappe et une chaîne de texte d’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="66769-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="66769-223">Lorsque la boîte de dialogue est créée, elle analyse le tableau et ajoute chaque chaîne de texte de frappe à la zone de liste déroulante **Sélectionner une séquence de touches** .</span><span class="sxs-lookup"><span data-stu-id="66769-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="66769-224">Quand l’utilisateur clique sur le bouton **OK** , la boîte de dialogue recherche la chaîne de texte de frappe sélectionnée et récupère la chaîne de texte d’accélérateur correspondante.</span><span class="sxs-lookup"><span data-stu-id="66769-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="66769-225">La boîte de dialogue ajoute la chaîne de texte d’accélérateur au texte de l’élément de menu sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66769-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="66769-226">L’exemple suivant montre le tableau de structures VKEY :</span><span class="sxs-lookup"><span data-stu-id="66769-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="66769-227">La procédure d’initialisation de la boîte de dialogue remplit l' **élément sélectionné** et sélectionne des zones de liste déroulante de **frappe** .</span><span class="sxs-lookup"><span data-stu-id="66769-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="66769-228">Une fois que l’utilisateur a sélectionné un élément de menu et un accélérateur associé, la boîte de dialogue examine les contrôles dans la boîte de dialogue pour obtenir la sélection de l’utilisateur, met à jour le texte de l’élément de menu, puis crée une nouvelle table d’accélérateurs qui contient le nouvel accélérateur défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66769-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="66769-229">L’exemple suivant illustre la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="66769-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="66769-230">Notez que vous devez initialiser dans votre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66769-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 