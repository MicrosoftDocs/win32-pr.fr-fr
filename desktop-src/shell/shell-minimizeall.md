---
description: Réduit toutes les fenêtres sur le bureau.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Shell. MinimizeAll, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973683"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="b2148-103">Shell. MinimizeAll, méthode</span><span class="sxs-lookup"><span data-stu-id="b2148-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="b2148-104">Réduit toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="b2148-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="b2148-105">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner **réduire toutes les fenêtres** sur les systèmes plus anciens ou de cliquer sur l’icône **afficher le bureau** dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2148-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2148-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2148-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="b2148-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2148-107">Parameters</span></span>

<span data-ttu-id="b2148-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b2148-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="b2148-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="b2148-109">Examples</span></span>

<span data-ttu-id="b2148-110">L’exemple suivant montre **MinimizeAll** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b2148-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="b2148-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b2148-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b2148-112">Langage</span><span class="sxs-lookup"><span data-stu-id="b2148-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="b2148-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="b2148-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b2148-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="b2148-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b2148-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b2148-115">Requirements</span></span>



| <span data-ttu-id="b2148-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2148-116">Requirement</span></span> | <span data-ttu-id="b2148-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2148-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2148-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2148-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2148-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2148-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b2148-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2148-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2148-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2148-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b2148-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2148-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2148-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2148-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b2148-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="b2148-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2148-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2148-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b2148-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b2148-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2148-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b2148-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2148-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2148-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2148-129">**Shell**</span><span class="sxs-lookup"><span data-stu-id="b2148-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="b2148-130">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="b2148-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




