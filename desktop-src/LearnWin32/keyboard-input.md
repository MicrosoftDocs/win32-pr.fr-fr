---
title: Entrée au clavier (prise en main de Win32 et C++)
description: Entrée au clavier
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "106540913"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="99ef9-103">Entrée au clavier (prise en main de Win32 et C++)</span><span class="sxs-lookup"><span data-stu-id="99ef9-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="99ef9-104">Le clavier est utilisé pour plusieurs types d’entrée distincts, notamment :</span><span class="sxs-lookup"><span data-stu-id="99ef9-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="99ef9-105">Entrée de caractères.</span><span class="sxs-lookup"><span data-stu-id="99ef9-105">Character input.</span></span> <span data-ttu-id="99ef9-106">Texte que l’utilisateur tape dans un document ou une zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="99ef9-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="99ef9-107">Raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="99ef9-107">Keyboard shortcuts.</span></span> <span data-ttu-id="99ef9-108">Séquences de touches qui appellent des fonctions d’application ; par exemple, appuyez sur CTRL + O pour ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="99ef9-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="99ef9-109">Commandes système.</span><span class="sxs-lookup"><span data-stu-id="99ef9-109">System commands.</span></span> <span data-ttu-id="99ef9-110">Séquences de touches qui appellent des fonctions système ; par exemple, ALT + TAB pour basculer entre les fenêtres.</span><span class="sxs-lookup"><span data-stu-id="99ef9-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="99ef9-111">Lorsque vous réfléchissez à l’entrée au clavier, il est important de se souvenir qu’un trait de touche n’est pas le même qu’un caractère.</span><span class="sxs-lookup"><span data-stu-id="99ef9-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="99ef9-112">Par exemple, si vous appuyez sur la touche A, vous obtenez l’un des caractères suivants.</span><span class="sxs-lookup"><span data-stu-id="99ef9-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="99ef9-113">a</span><span class="sxs-lookup"><span data-stu-id="99ef9-113">a</span></span>
-   <span data-ttu-id="99ef9-114">A</span><span class="sxs-lookup"><span data-stu-id="99ef9-114">A</span></span>
-   <span data-ttu-id="99ef9-115">á (si le clavier prend en charge la combinaison de signes diacritiques)</span><span class="sxs-lookup"><span data-stu-id="99ef9-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="99ef9-116">En outre, si la touche ALT est maintenue enfoncée, le fait d’appuyer sur une touche A produit ALT + A, que le système ne considère pas comme un caractère, mais plutôt comme une commande système.</span><span class="sxs-lookup"><span data-stu-id="99ef9-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="99ef9-117">Codes de touche</span><span class="sxs-lookup"><span data-stu-id="99ef9-117">Key Codes</span></span>

<span data-ttu-id="99ef9-118">Lorsque vous appuyez sur une touche, le matériel génère un *code d’analyse*.</span><span class="sxs-lookup"><span data-stu-id="99ef9-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="99ef9-119">Les codes d’analyse varient d’un clavier à l’autre, et il existe des codes d’analyse distincts pour les événements de touche et de réduction de la clé.</span><span class="sxs-lookup"><span data-stu-id="99ef9-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="99ef9-120">Vous n’aurez presque jamais à vous soucier des codes d’analyse.</span><span class="sxs-lookup"><span data-stu-id="99ef9-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="99ef9-121">Le pilote de clavier traduit les codes d’analyse en *codes de clé virtuelle*.</span><span class="sxs-lookup"><span data-stu-id="99ef9-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="99ef9-122">Les codes de clé virtuelle sont indépendants des appareils.</span><span class="sxs-lookup"><span data-stu-id="99ef9-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="99ef9-123">Si vous appuyez sur la touche A sur n’importe quel clavier, vous générez le même code de clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="99ef9-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="99ef9-124">En général, les codes de clé virtuelle ne correspondent pas aux codes ASCII ou à toute autre norme d’encodage de caractères.</span><span class="sxs-lookup"><span data-stu-id="99ef9-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="99ef9-125">Cela est évident si vous y réfléchissez, car la même clé peut générer des caractères différents (a, A, á) et certaines clés, telles que les touches de fonction, ne correspondent à aucun caractère.</span><span class="sxs-lookup"><span data-stu-id="99ef9-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="99ef9-126">Cela dit, les codes de clé virtuelle suivants sont mappés à des équivalents ASCII :</span><span class="sxs-lookup"><span data-stu-id="99ef9-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="99ef9-127">0 à 9 clés = ASCII « 0 » – « 9 » (0x30 – 0x39)</span><span class="sxs-lookup"><span data-stu-id="99ef9-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="99ef9-128">A à Z, clés = ASCII’A' – 'Z' (0x41 vers – 0x5A)</span><span class="sxs-lookup"><span data-stu-id="99ef9-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="99ef9-129">Dans certains cas, ce mappage est malheureux, car vous ne devriez jamais considérer les codes de clé virtuelle comme des caractères, pour les raisons évoquées.</span><span class="sxs-lookup"><span data-stu-id="99ef9-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="99ef9-130">Le fichier d’en-tête WinUser. h définit des constantes pour la plupart des codes de touche virtuelle.</span><span class="sxs-lookup"><span data-stu-id="99ef9-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="99ef9-131">Par exemple, le code de touche virtuelle pour la touche de direction gauche est **VK \_ gauche** (0x25).</span><span class="sxs-lookup"><span data-stu-id="99ef9-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="99ef9-132">Pour obtenir la liste complète des codes de touche virtuelle, consultez la section [**codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="99ef9-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="99ef9-133">Aucune constante n’est définie pour les codes de clé virtuelle qui correspondent aux valeurs ASCII.</span><span class="sxs-lookup"><span data-stu-id="99ef9-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="99ef9-134">Par exemple, le code de la touche virtuelle pour la clé A est 0x41 vers, mais il n’existe aucune constante nommée **VK \_ a**.</span><span class="sxs-lookup"><span data-stu-id="99ef9-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="99ef9-135">Au lieu de cela, utilisez simplement la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="99ef9-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="99ef9-136">Messages Key-Down et Key-Up</span><span class="sxs-lookup"><span data-stu-id="99ef9-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="99ef9-137">Lorsque vous appuyez sur une touche, la fenêtre qui a le focus clavier reçoit l’un des messages suivants.</span><span class="sxs-lookup"><span data-stu-id="99ef9-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="99ef9-138">**\_SYSKEYDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="99ef9-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="99ef9-139">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="99ef9-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="99ef9-140">Le message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indique une *clé système*, qui est un trait de clé qui appelle une commande système.</span><span class="sxs-lookup"><span data-stu-id="99ef9-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="99ef9-141">Il existe deux types de clé système :</span><span class="sxs-lookup"><span data-stu-id="99ef9-141">There are two types of system key:</span></span>

-   <span data-ttu-id="99ef9-142">ALT + n’importe quelle touche</span><span class="sxs-lookup"><span data-stu-id="99ef9-142">ALT + any key</span></span>
-   <span data-ttu-id="99ef9-143">F10</span><span class="sxs-lookup"><span data-stu-id="99ef9-143">F10</span></span>

<span data-ttu-id="99ef9-144">La touche F10 active la barre de menus d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="99ef9-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="99ef9-145">Différentes combinaisons de touches ALT appellent des commandes système.</span><span class="sxs-lookup"><span data-stu-id="99ef9-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="99ef9-146">Par exemple, ALT + TAB bascule vers une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="99ef9-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="99ef9-147">En outre, si une fenêtre possède un menu, la touche ALT peut être utilisée pour activer les éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="99ef9-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="99ef9-148">Certaines combinaisons de touches ALT ne font rien.</span><span class="sxs-lookup"><span data-stu-id="99ef9-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="99ef9-149">Tous les autres raccourcis clavier sont considérés comme des clés qui ne sont pas des clés système et produisent le message [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut.</span><span class="sxs-lookup"><span data-stu-id="99ef9-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="99ef9-150">Cela comprend les touches de fonction autres que F10.</span><span class="sxs-lookup"><span data-stu-id="99ef9-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="99ef9-151">Lorsque vous publiez une clé, le système envoie un message de clé correspondant :</span><span class="sxs-lookup"><span data-stu-id="99ef9-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="99ef9-152">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="99ef9-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="99ef9-153">**\_SYSKEYUP WM**</span><span class="sxs-lookup"><span data-stu-id="99ef9-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="99ef9-154">Si vous maintenez la touche enfoncée suffisamment longtemps pour démarrer la fonctionnalité répéter du clavier, le système envoie plusieurs messages de déverrouillage, suivis d’un seul message de clé.</span><span class="sxs-lookup"><span data-stu-id="99ef9-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="99ef9-155">Dans les quatre messages de clavier abordés jusqu’à présent, le paramètre *wParam* contient le code de clé virtuelle de la clé.</span><span class="sxs-lookup"><span data-stu-id="99ef9-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="99ef9-156">Le paramètre *lParam* contient des informations diverses compressées dans 32 bits.</span><span class="sxs-lookup"><span data-stu-id="99ef9-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="99ef9-157">En général, vous n’avez pas besoin des informations contenues dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="99ef9-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="99ef9-158">Un indicateur qui peut être utile est le bit 30, l’indicateur « état de la clé précédent », qui est défini sur 1 pour les messages de déverrouillage répétés.</span><span class="sxs-lookup"><span data-stu-id="99ef9-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="99ef9-159">Comme son nom l’indique, les séquences de touches système sont principalement destinées à être utilisées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="99ef9-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="99ef9-160">Si vous interceptez le message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) , appelez [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) par la suite.</span><span class="sxs-lookup"><span data-stu-id="99ef9-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="99ef9-161">Dans le cas contraire, vous empêchez le système d’exploitation de gérer la commande.</span><span class="sxs-lookup"><span data-stu-id="99ef9-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="99ef9-162">Messages de caractères</span><span class="sxs-lookup"><span data-stu-id="99ef9-162">Character Messages</span></span>

<span data-ttu-id="99ef9-163">Les séquences de touches sont converties en caractères à l’aide de la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , que nous avons constatée pour la première fois dans le [module 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="99ef9-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="99ef9-164">Cette fonction examine les messages dépendants et les convertit en caractères.</span><span class="sxs-lookup"><span data-stu-id="99ef9-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="99ef9-165">Pour chaque caractère produit, la fonction **TranslateMessage** place un message [**WM \_**](/windows/desktop/inputdev/wm-char) ou [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) dans la file d’attente de messages de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="99ef9-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="99ef9-166">Le paramètre *wParam* du message contient le caractère UTF-16.</span><span class="sxs-lookup"><span data-stu-id="99ef9-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="99ef9-167">Comme vous pouvez le deviner, les messages [**WM \_ char**](/windows/desktop/inputdev/wm-char) sont générés à partir des messages [**\_ WM**](/windows/desktop/inputdev/wm-keydown) KeyOut, tandis que les messages [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) sont générés à partir des messages [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) .</span><span class="sxs-lookup"><span data-stu-id="99ef9-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="99ef9-168">Par exemple, supposons que l’utilisateur appuie sur la touche Maj suivie de la touche A.</span><span class="sxs-lookup"><span data-stu-id="99ef9-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="99ef9-169">En supposant une disposition de clavier standard, vous obtiendriez la séquence de messages suivante :</span><span class="sxs-lookup"><span data-stu-id="99ef9-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="99ef9-170">**WM \_ touche PG. suiv**.</span><span class="sxs-lookup"><span data-stu-id="99ef9-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="99ef9-171">**WM \_ keyverser**: A</span><span class="sxs-lookup"><span data-stu-id="99ef9-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="99ef9-172">**WM \_ CHAR**: 'A'</span><span class="sxs-lookup"><span data-stu-id="99ef9-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="99ef9-173">En revanche, la combinaison ALT + P générerait :</span><span class="sxs-lookup"><span data-stu-id="99ef9-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="99ef9-174">**WM \_ SYSKEYDOWN**: \_ menu VK</span><span class="sxs-lookup"><span data-stu-id="99ef9-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="99ef9-175">**WM \_ SYSKEYDOWN**: 0x50</span><span class="sxs-lookup"><span data-stu-id="99ef9-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="99ef9-176">**WM \_ SYSCHAR**: « p »</span><span class="sxs-lookup"><span data-stu-id="99ef9-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="99ef9-177">**WM \_ SYSKEYUP**: 0x50</span><span class="sxs-lookup"><span data-stu-id="99ef9-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="99ef9-178">**WM \_ KEYUP**: \_ menu VK</span><span class="sxs-lookup"><span data-stu-id="99ef9-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="99ef9-179">(Le code de touche virtuelle pour la touche ALT est appelé VK \_ MENU pour des raisons historiques.)</span><span class="sxs-lookup"><span data-stu-id="99ef9-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="99ef9-180">Le message [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) indique un caractère système.</span><span class="sxs-lookup"><span data-stu-id="99ef9-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="99ef9-181">Comme avec [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), vous devez généralement transmettre ce message directement à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="99ef9-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="99ef9-182">Dans le cas contraire, vous risquez d’interférer avec les commandes système standard.</span><span class="sxs-lookup"><span data-stu-id="99ef9-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="99ef9-183">En particulier, ne traitez pas **WM \_ SYSCHAR** comme du texte que l’utilisateur a tapé.</span><span class="sxs-lookup"><span data-stu-id="99ef9-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="99ef9-184">Le message [**WM \_ char**](/windows/desktop/inputdev/wm-char) correspond à ce que vous considérez normalement comme une entrée de caractères.</span><span class="sxs-lookup"><span data-stu-id="99ef9-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="99ef9-185">Le type de données pour le caractère est **WCHAR \_ t**, qui représente un caractère Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="99ef9-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="99ef9-186">L’entrée de caractères peut inclure des caractères en dehors de la plage ASCII, en particulier avec les dispositions de clavier qui sont couramment utilisées en dehors de la États-Unis.</span><span class="sxs-lookup"><span data-stu-id="99ef9-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="99ef9-187">Vous pouvez essayer différentes dispositions du clavier en installant un clavier régional, puis en utilisant la fonctionnalité du clavier visuel.</span><span class="sxs-lookup"><span data-stu-id="99ef9-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="99ef9-188">Les utilisateurs peuvent également installer un éditeur de méthode d’entrée (IME) pour entrer des scripts complexes, tels que des caractères japonais, à l’aide d’un clavier standard.</span><span class="sxs-lookup"><span data-stu-id="99ef9-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="99ef9-189">Par exemple, en utilisant un IME japonais pour entrer le caractère katakana カ (Ka), vous pouvez obtenir les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="99ef9-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="99ef9-190">**WM \_ Keyverse**: VK \_ PROCESSKEY (clé de processus IME)</span><span class="sxs-lookup"><span data-stu-id="99ef9-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="99ef9-191">**WM \_ KEYUP**: 0x4B</span><span class="sxs-lookup"><span data-stu-id="99ef9-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="99ef9-192">**WM \_ keyverse**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="99ef9-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="99ef9-193">**WM \_ KEYUP**: 0x41 vers</span><span class="sxs-lookup"><span data-stu-id="99ef9-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="99ef9-194">**WM \_ keyverse**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="99ef9-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="99ef9-195">**WM \_ CHAR**: カ</span><span class="sxs-lookup"><span data-stu-id="99ef9-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="99ef9-196">**WM \_ KEYUP**: \_ retour VK</span><span class="sxs-lookup"><span data-stu-id="99ef9-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="99ef9-197">Certaines combinaisons de touches CTRL sont converties en caractères de contrôle ASCII.</span><span class="sxs-lookup"><span data-stu-id="99ef9-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="99ef9-198">Par exemple, CTRL + A est converti en caractère ASCII Ctrl-A (SOH) (valeur ASCII 0x01).</span><span class="sxs-lookup"><span data-stu-id="99ef9-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="99ef9-199">Pour l’entrée de texte, vous devez généralement filtrer les caractères de contrôle.</span><span class="sxs-lookup"><span data-stu-id="99ef9-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="99ef9-200">Évitez également d’utiliser [**WM \_ char**](/windows/desktop/inputdev/wm-char) pour implémenter des raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="99ef9-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="99ef9-201">Au lieu de cela, utilisez des messages de [**\_ keyversion WM**](/windows/desktop/inputdev/wm-keydown) ou bien mieux, utilisez une table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="99ef9-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="99ef9-202">Les tables d’accélérateurs sont décrites dans la rubrique suivante, [tables d’accélérateurs](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="99ef9-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="99ef9-203">Le code suivant affiche les principaux messages du clavier dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="99ef9-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="99ef9-204">Essayez d’utiliser différentes combinaisons de touches et consultez les messages générés.</span><span class="sxs-lookup"><span data-stu-id="99ef9-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="99ef9-205">Divers messages de clavier</span><span class="sxs-lookup"><span data-stu-id="99ef9-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="99ef9-206">Certains autres messages de clavier peuvent être ignorés en toute sécurité par la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="99ef9-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="99ef9-207">Le message [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) est envoyé pour une clé de combinaison, telle qu’un signe diacritique.</span><span class="sxs-lookup"><span data-stu-id="99ef9-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="99ef9-208">Par exemple, sur un clavier en espagnol, si vous tapez accent (') suivi de E, vous obtenez le caractère é.</span><span class="sxs-lookup"><span data-stu-id="99ef9-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="99ef9-209">Le **\_ DEADCHAR WM** est envoyé pour le caractère d’accentuation.</span><span class="sxs-lookup"><span data-stu-id="99ef9-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="99ef9-210">Le message [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) est obsolète.</span><span class="sxs-lookup"><span data-stu-id="99ef9-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="99ef9-211">Il permet aux programmes ANSI de recevoir l’entrée de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="99ef9-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="99ef9-212">Le caractère de caractère [**\_ \_ IME WM**](/windows/desktop/Intl/wm-ime-char) est envoyé lorsqu’un IME traduit une séquence de frappe en caractères.</span><span class="sxs-lookup"><span data-stu-id="99ef9-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="99ef9-213">Il est envoyé en plus du message [**WM habituel \_**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="99ef9-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="99ef9-214">État du clavier</span><span class="sxs-lookup"><span data-stu-id="99ef9-214">Keyboard State</span></span>

<span data-ttu-id="99ef9-215">Les messages de clavier sont pilotés par les événements.</span><span class="sxs-lookup"><span data-stu-id="99ef9-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="99ef9-216">Autrement dit, vous recevez un message quand un événement intéressant se produit, par exemple une pression sur une touche, et le message vous indique ce qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="99ef9-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="99ef9-217">Toutefois, vous pouvez également tester l’état d’une clé à tout moment, en appelant la fonction [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="99ef9-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="99ef9-218">Par exemple, réfléchissez à la façon dont vous allez détecter la combinaison du bouton gauche de la souris et de la touche ALT.</span><span class="sxs-lookup"><span data-stu-id="99ef9-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="99ef9-219">Vous pouvez suivre l’état de la touche ALT en écoutant les messages de frappe de touche et en stockant un indicateur, mais [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) vous évite les problèmes.</span><span class="sxs-lookup"><span data-stu-id="99ef9-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="99ef9-220">Quand vous recevez le message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , il vous suffit d’appeler **GetKeyState** comme suit :</span><span class="sxs-lookup"><span data-stu-id="99ef9-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="99ef9-221">Le message [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) prend un code de touche virtuelle comme entrée et retourne un jeu d’indicateurs binaires (en réalité, il s’agit simplement de deux indicateurs).</span><span class="sxs-lookup"><span data-stu-id="99ef9-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="99ef9-222">La valeur 0x8000 contient l’indicateur binaire qui teste si la touche est actuellement enfoncée.</span><span class="sxs-lookup"><span data-stu-id="99ef9-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="99ef9-223">La plupart des claviers ont deux touches ALT, gauche et droite.</span><span class="sxs-lookup"><span data-stu-id="99ef9-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="99ef9-224">L’exemple précédent teste si l’un de ces éléments est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="99ef9-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="99ef9-225">Vous pouvez également utiliser [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) pour faire la distinction entre les instances de gauche et de droite des touches Alt, Maj ou Ctrl.</span><span class="sxs-lookup"><span data-stu-id="99ef9-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="99ef9-226">Par exemple, le code suivant teste si la touche ALT droite est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="99ef9-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="99ef9-227">La fonction [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) est intéressante, car elle signale un État du clavier *virtuel* .</span><span class="sxs-lookup"><span data-stu-id="99ef9-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="99ef9-228">Cet État virtuel est basé sur le contenu de la file d’attente de messages et est mis à jour lorsque vous supprimez des messages de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="99ef9-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="99ef9-229">Au fur et à mesure que votre programme traite des messages de fenêtre, **GetKeyState** vous donne un instantané du clavier au moment où chaque message a été mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="99ef9-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="99ef9-230">Par exemple, si le dernier message de la file d’attente était [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** signale l’état du clavier au moment où l’utilisateur clique sur le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="99ef9-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="99ef9-231">Étant donné que [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) est basé sur la file d’attente de messages, il ignore également l’entrée au clavier qui a été envoyée à un autre programme.</span><span class="sxs-lookup"><span data-stu-id="99ef9-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="99ef9-232">Si l’utilisateur bascule vers un autre programme, toute pression sur les touches qui sont envoyées à ce programme est ignorée par **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="99ef9-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="99ef9-233">Si vous souhaitez vraiment connaître l’état physique immédiat du clavier, il existe une fonction pour cela : [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="99ef9-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="99ef9-234">Toutefois, pour la plupart du code d’interface utilisateur, la fonction correcte est **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="99ef9-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="99ef9-235">Suivant</span><span class="sxs-lookup"><span data-stu-id="99ef9-235">Next</span></span>

[<span data-ttu-id="99ef9-236">Tables d’accélérateurs</span><span class="sxs-lookup"><span data-stu-id="99ef9-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
