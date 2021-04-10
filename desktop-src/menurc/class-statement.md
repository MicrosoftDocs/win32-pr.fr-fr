---
title: Instruction de classe
description: Définit la classe de la boîte de dialogue.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menus de l’instruction de classe et autres ressources
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940924"
---
# <a name="class-statement"></a><span data-ttu-id="c33e5-104">Instruction de classe</span><span class="sxs-lookup"><span data-stu-id="c33e5-104">CLASS statement</span></span>

<span data-ttu-id="c33e5-105">Définit la classe de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c33e5-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="c33e5-106">L’instruction de **classe** s’affiche dans la section facultative avant l’instruction main de la [**boîte de dialogue**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="c33e5-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="c33e5-107">Si aucune classe n’est fournie, la classe de boîte de dialogue standard est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c33e5-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="c33e5-108"><span id="class"></span><span id="CLASS"></span>*type*</span><span class="sxs-lookup"><span data-stu-id="c33e5-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="c33e5-109">Entier non signé 16 bits ou chaîne, placé entre guillemets doubles ("), qui identifie la classe de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c33e5-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="c33e5-110">Si la procédure de fenêtre pour la classe ne traite pas un message qui lui est envoyé, elle doit appeler la fonction [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) pour s’assurer que tous les messages sont correctement gérés pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c33e5-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="c33e5-111">Une classe privée peut utiliser **DefDlgProc** comme procédure de fenêtre par défaut.</span><span class="sxs-lookup"><span data-stu-id="c33e5-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="c33e5-112">La classe doit être inscrite avec le membre **cbWndExtra** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) définie sur **DLGWINDOWEXTRA**.</span><span class="sxs-lookup"><span data-stu-id="c33e5-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c33e5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c33e5-113">Remarks</span></span>

<span data-ttu-id="c33e5-114">L’instruction **Class** ne doit être utilisée qu’avec des cas spéciaux, car elle remplace le traitement normal d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c33e5-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="c33e5-115">L’instruction de **classe** convertit une boîte de dialogue en une fenêtre de la classe spécifiée ; en fonction de la classe, cela peut entraîner des résultats indésirables.</span><span class="sxs-lookup"><span data-stu-id="c33e5-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="c33e5-116">N’utilisez pas les noms de classe de contrôle redéfinis avec cette instruction.</span><span class="sxs-lookup"><span data-stu-id="c33e5-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="c33e5-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c33e5-117">Examples</span></span>

<span data-ttu-id="c33e5-118">L’exemple suivant illustre l’utilisation de l’instruction de **classe** :</span><span class="sxs-lookup"><span data-stu-id="c33e5-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="c33e5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c33e5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33e5-120">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="c33e5-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="c33e5-121">**DIALOGUE**</span><span class="sxs-lookup"><span data-stu-id="c33e5-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 