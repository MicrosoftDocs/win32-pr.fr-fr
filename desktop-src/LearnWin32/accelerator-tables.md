---
title: Tables d’accélérateurs
description: Tables d’accélérateurs
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2951ee99a31a977e0909de5639fa3110cea10e0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090817"
---
# <a name="accelerator-tables"></a><span data-ttu-id="58c2c-103">Tables d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="58c2c-103">Accelerator Tables</span></span>

<span data-ttu-id="58c2c-104">Les applications définissent souvent des raccourcis clavier, tels que CTRL + O pour la commande fichier ouvrir.</span><span class="sxs-lookup"><span data-stu-id="58c2c-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="58c2c-105">Vous pouvez implémenter des raccourcis clavier en gérant des messages de [**\_ keyversion WM**](/windows/desktop/inputdev/wm-keydown) individuels, mais les tables d’accélérateurs offrent une meilleure solution :</span><span class="sxs-lookup"><span data-stu-id="58c2c-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="58c2c-106">Nécessite moins de codage.</span><span class="sxs-lookup"><span data-stu-id="58c2c-106">Requires less coding.</span></span>
-   <span data-ttu-id="58c2c-107">Consolide tous vos raccourcis dans un seul fichier de données.</span><span class="sxs-lookup"><span data-stu-id="58c2c-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="58c2c-108">Prend en charge la localisation dans d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="58c2c-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="58c2c-109">Permet aux raccourcis et aux commandes de menu d’utiliser la même logique d’application.</span><span class="sxs-lookup"><span data-stu-id="58c2c-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="58c2c-110">Une *table d’accélérateurs* est une ressource de données qui mappe les combinaisons de touches de clavier, telles que CTRL + O, aux commandes de l’application.</span><span class="sxs-lookup"><span data-stu-id="58c2c-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="58c2c-111">Avant de voir comment utiliser une table d’accélérateurs, nous aurons besoin d’une présentation rapide des ressources.</span><span class="sxs-lookup"><span data-stu-id="58c2c-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="58c2c-112">Une *ressource* est un objet blob de données qui est intégré à un fichier binaire d’application (exe ou dll).</span><span class="sxs-lookup"><span data-stu-id="58c2c-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="58c2c-113">Les ressources stockent des données qui sont nécessaires à l’application, telles que des menus, des curseurs, des icônes, des images, des chaînes de texte ou des données d’application personnalisées.</span><span class="sxs-lookup"><span data-stu-id="58c2c-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="58c2c-114">L’application charge les données de ressources à partir du fichier binaire au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="58c2c-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="58c2c-115">Pour inclure des ressources dans un fichier binaire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="58c2c-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="58c2c-116">Créez un fichier de définition de ressource (. RC).</span><span class="sxs-lookup"><span data-stu-id="58c2c-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="58c2c-117">Ce fichier définit les types de ressources et leurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="58c2c-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="58c2c-118">Le fichier de définition de ressource peut inclure des références à d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="58c2c-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="58c2c-119">Par exemple, une ressource icône est déclarée dans le fichier. RC, mais l’image d’icône est stockée dans un fichier séparé.</span><span class="sxs-lookup"><span data-stu-id="58c2c-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="58c2c-120">Utilisez le compilateur de ressources Microsoft Windows (RC) pour compiler le fichier de définition de ressource dans un fichier de ressources (. res) compilé.</span><span class="sxs-lookup"><span data-stu-id="58c2c-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="58c2c-121">Le compilateur RC est fourni avec Visual Studio, ainsi que le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="58c2c-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="58c2c-122">Liez le fichier de ressources compilé au fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="58c2c-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="58c2c-123">Ces étapes sont à peu près équivalentes au processus de compilation/liaison pour les fichiers de code.</span><span class="sxs-lookup"><span data-stu-id="58c2c-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="58c2c-124">Visual Studio fournit un ensemble d’éditeurs de ressources qui facilitent la création et la modification des ressources.</span><span class="sxs-lookup"><span data-stu-id="58c2c-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="58c2c-125">(Ces outils ne sont pas disponibles dans les éditions Express de Visual Studio.) Mais un fichier. RC est simplement un fichier texte et la syntaxe est documentée sur MSDN. il est donc possible de créer un fichier. RC à l’aide de n’importe quel éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="58c2c-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="58c2c-126">Pour plus d’informations, consultez [à propos des fichiers de ressources](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="58c2c-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="58c2c-127">Définition d’une table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="58c2c-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="58c2c-128">Une table d’accélérateurs est un tableau de raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="58c2c-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="58c2c-129">Chaque raccourci est défini par :</span><span class="sxs-lookup"><span data-stu-id="58c2c-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="58c2c-130">Identificateur numérique.</span><span class="sxs-lookup"><span data-stu-id="58c2c-130">A numeric identifier.</span></span> <span data-ttu-id="58c2c-131">Ce nombre identifie la commande d’application qui sera appelée par le raccourci.</span><span class="sxs-lookup"><span data-stu-id="58c2c-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="58c2c-132">Caractère ASCII ou code de touche virtuelle du raccourci.</span><span class="sxs-lookup"><span data-stu-id="58c2c-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="58c2c-133">Touches de modification facultatives : ALT, Maj ou CTRL.</span><span class="sxs-lookup"><span data-stu-id="58c2c-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="58c2c-134">La table d’accélérateurs elle-même a un identificateur numérique, qui identifie la table dans la liste des ressources d’application.</span><span class="sxs-lookup"><span data-stu-id="58c2c-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="58c2c-135">Nous allons créer une table d’accélérateurs pour un programme de dessin simple.</span><span class="sxs-lookup"><span data-stu-id="58c2c-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="58c2c-136">Ce programme aura deux modes, le mode dessin et le mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="58c2c-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="58c2c-137">En mode dessin, l’utilisateur peut dessiner des formes.</span><span class="sxs-lookup"><span data-stu-id="58c2c-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="58c2c-138">En mode de sélection, l’utilisateur peut sélectionner des formes.</span><span class="sxs-lookup"><span data-stu-id="58c2c-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="58c2c-139">Pour ce programme, nous souhaitons définir les raccourcis clavier suivants.</span><span class="sxs-lookup"><span data-stu-id="58c2c-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="58c2c-140">Raccourci</span><span class="sxs-lookup"><span data-stu-id="58c2c-140">Shortcut</span></span> | <span data-ttu-id="58c2c-141">Commande</span><span class="sxs-lookup"><span data-stu-id="58c2c-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="58c2c-142">Ctrl+M</span><span class="sxs-lookup"><span data-stu-id="58c2c-142">CTRL+M</span></span>   | <span data-ttu-id="58c2c-143">Basculer entre les modes.</span><span class="sxs-lookup"><span data-stu-id="58c2c-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="58c2c-144">F1</span><span class="sxs-lookup"><span data-stu-id="58c2c-144">F1</span></span>       | <span data-ttu-id="58c2c-145">Basculez en mode dessin.</span><span class="sxs-lookup"><span data-stu-id="58c2c-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="58c2c-146">F2</span><span class="sxs-lookup"><span data-stu-id="58c2c-146">F2</span></span>       | <span data-ttu-id="58c2c-147">Basculez en mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="58c2c-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="58c2c-148">Tout d’abord, définissez des identificateurs numériques pour la table et pour les commandes de l’application.</span><span class="sxs-lookup"><span data-stu-id="58c2c-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="58c2c-149">Ces valeurs sont arbitraires.</span><span class="sxs-lookup"><span data-stu-id="58c2c-149">These values are arbitrary.</span></span> <span data-ttu-id="58c2c-150">Vous pouvez assigner des constantes symboliques pour les identificateurs en les définissant dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="58c2c-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="58c2c-151">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="58c2c-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="58c2c-152">Dans cet exemple, la valeur `IDR_ACCEL1` identifie la table d’accélérateurs, et les trois constantes suivantes définissent les commandes de l’application.</span><span class="sxs-lookup"><span data-stu-id="58c2c-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="58c2c-153">Par Convention, un fichier d’en-tête qui définit les constantes de ressource est souvent nommé Resource. h.</span><span class="sxs-lookup"><span data-stu-id="58c2c-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="58c2c-154">La liste suivante montre le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="58c2c-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="58c2c-155">Les raccourcis d’accélérateur sont définis à l’intérieur des accolades.</span><span class="sxs-lookup"><span data-stu-id="58c2c-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="58c2c-156">Chaque raccourci contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="58c2c-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="58c2c-157">Code de la touche virtuelle ou caractère ASCII qui appelle le raccourci.</span><span class="sxs-lookup"><span data-stu-id="58c2c-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="58c2c-158">Commande de l’application.</span><span class="sxs-lookup"><span data-stu-id="58c2c-158">The application command.</span></span> <span data-ttu-id="58c2c-159">Notez que les constantes symboliques sont utilisées dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="58c2c-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="58c2c-160">Le fichier de définition de ressource contient Resource. h, où ces constantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="58c2c-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="58c2c-161">Le mot clé **VIRTKEY** signifie que la première entrée est un code de touche virtuelle.</span><span class="sxs-lookup"><span data-stu-id="58c2c-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="58c2c-162">L’autre option consiste à utiliser des caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="58c2c-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="58c2c-163">Modificateurs facultatifs : ALT, CTRL ou Maj.</span><span class="sxs-lookup"><span data-stu-id="58c2c-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="58c2c-164">Si vous utilisez des caractères ASCII pour les raccourcis, un caractère minuscule est un raccourci différent de celui d’un caractère majuscule.</span><span class="sxs-lookup"><span data-stu-id="58c2c-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="58c2c-165">(Par exemple, si vous tapez’a', vous pouvez appeler une commande différente de la saisie de’A'.) Comme cela peut entraîner une confusion pour les utilisateurs, il est généralement préférable d’utiliser des codes de touche virtuelle, plutôt que des caractères ASCII, pour les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="58c2c-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="58c2c-166">Chargement de la table d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="58c2c-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="58c2c-167">La ressource de la table d’accélérateurs doit être chargée pour que le programme puisse l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="58c2c-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="58c2c-168">Pour charger une table d’accélérateurs, appelez la fonction [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .</span><span class="sxs-lookup"><span data-stu-id="58c2c-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="58c2c-169">Appelez cette fonction avant d’entrer dans la boucle de message.</span><span class="sxs-lookup"><span data-stu-id="58c2c-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="58c2c-170">Le premier paramètre est le handle du module.</span><span class="sxs-lookup"><span data-stu-id="58c2c-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="58c2c-171">(Ce paramètre est passé à votre fonction [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="58c2c-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="58c2c-172">Pour plus d’informations, consultez [WinMain : le point d’entrée de l’application](winmain--the-application-entry-point.md).) Le deuxième paramètre est l’identificateur de ressource.</span><span class="sxs-lookup"><span data-stu-id="58c2c-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="58c2c-173">La fonction retourne un handle vers la ressource.</span><span class="sxs-lookup"><span data-stu-id="58c2c-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="58c2c-174">Rappelez-vous qu’un handle est un type opaque qui fait référence à un objet géré par le système.</span><span class="sxs-lookup"><span data-stu-id="58c2c-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="58c2c-175">Si la fonction échoue, elle retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="58c2c-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="58c2c-176">Vous pouvez publier une table d’accélérateurs en appelant [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span><span class="sxs-lookup"><span data-stu-id="58c2c-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="58c2c-177">Toutefois, le système libère automatiquement la table lorsque le programme s’arrête. vous devez donc appeler cette fonction uniquement si vous remplacez une table par une autre.</span><span class="sxs-lookup"><span data-stu-id="58c2c-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="58c2c-178">Un exemple intéressant de cela est illustré dans la rubrique [création d’accélérateurs modifiables](/windows/desktop/menurc/using-keyboard-accelerators)par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58c2c-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="58c2c-179">Conversion des frappes de touches en commandes</span><span class="sxs-lookup"><span data-stu-id="58c2c-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="58c2c-180">Une table d’accélérateurs fonctionne en traduisant les séquences de touches en messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="58c2c-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="58c2c-181">Le paramètre *wParam* de **la \_ commande WM** contient l’identificateur numérique de la commande.</span><span class="sxs-lookup"><span data-stu-id="58c2c-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="58c2c-182">Par exemple, à l’aide du tableau ci-dessus, le trait de touche CTRL + M est converti en message de **\_ commande WM** avec la valeur `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="58c2c-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="58c2c-183">Pour ce faire, remplacez votre boucle de message par la suivante :</span><span class="sxs-lookup"><span data-stu-id="58c2c-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="58c2c-184">Ce code ajoute un appel à la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) à l’intérieur de la boucle de message.</span><span class="sxs-lookup"><span data-stu-id="58c2c-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="58c2c-185">La fonction **TranslateAccelerator** examine chaque message de fenêtre, en recherchant des messages dépendants.</span><span class="sxs-lookup"><span data-stu-id="58c2c-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="58c2c-186">Si l’utilisateur appuie sur l’une des combinaisons de touches listées dans la table d’accélérateurs, **TranslateAccelerator** envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="58c2c-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="58c2c-187">La fonction envoie **la \_ commande WM** en appelant directement la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="58c2c-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="58c2c-188">Lorsque **TranslateAccelerator** convertit correctement un trait de touche, la fonction retourne une valeur différente de zéro, ce qui signifie que vous devez ignorer le traitement normal pour le message.</span><span class="sxs-lookup"><span data-stu-id="58c2c-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="58c2c-189">Sinon, **TranslateAccelerator** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="58c2c-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="58c2c-190">Dans ce cas, transmettez le message de fenêtre à [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) et [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), normalement.</span><span class="sxs-lookup"><span data-stu-id="58c2c-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="58c2c-191">Voici comment le programme de dessin peut gérer le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) :</span><span class="sxs-lookup"><span data-stu-id="58c2c-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="58c2c-192">Ce code suppose que `SetMode` est une fonction définie par l’application pour basculer entre les deux modes.</span><span class="sxs-lookup"><span data-stu-id="58c2c-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="58c2c-193">Les détails de la façon dont vous géreriez chaque commande dépendent évidemment de votre programme.</span><span class="sxs-lookup"><span data-stu-id="58c2c-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="58c2c-194">Suivant</span><span class="sxs-lookup"><span data-stu-id="58c2c-194">Next</span></span>

[<span data-ttu-id="58c2c-195">Définition de l’image de curseur</span><span class="sxs-lookup"><span data-stu-id="58c2c-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 
