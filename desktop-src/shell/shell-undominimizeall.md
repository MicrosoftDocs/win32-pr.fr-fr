---
description: Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande MinimizeAll.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Shell. UndoMinimizeALL, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203433"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="d7bb6-103">Shell. UndoMinimizeALL, méthode</span><span class="sxs-lookup"><span data-stu-id="d7bb6-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="d7bb6-104">Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bb6-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="d7bb6-105">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez **Annuler réduire toutes les fenêtres** sur les systèmes plus anciens ou un second clic sur l’icône **afficher le bureau** dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bb6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7bb6-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="d7bb6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7bb6-107">Parameters</span></span>

<span data-ttu-id="d7bb6-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="d7bb6-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="d7bb6-109">Examples</span></span>

<span data-ttu-id="d7bb6-110">L’exemple suivant montre **UndoMinimizeALL** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="d7bb6-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d7bb6-112">Langage</span><span class="sxs-lookup"><span data-stu-id="d7bb6-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="d7bb6-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="d7bb6-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d7bb6-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="d7bb6-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d7bb6-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7bb6-115">Requirements</span></span>



| <span data-ttu-id="d7bb6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7bb6-116">Requirement</span></span> | <span data-ttu-id="d7bb6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7bb6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bb6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bb6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bb6-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bb6-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7bb6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bb6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bb6-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bb6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d7bb6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7bb6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7bb6-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bb6-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d7bb6-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="d7bb6-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7bb6-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7bb6-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d7bb6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d7bb6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7bb6-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d7bb6-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




