---
description: Restaure toutes les fenêtres de bureau à l’État où elles se trouvaient avant la dernière commande MinimizeAll.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Méthode IShellDispatch. UndoMinimizeALL (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527333"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="02262-103">Méthode IShellDispatch. UndoMinimizeALL</span><span class="sxs-lookup"><span data-stu-id="02262-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="02262-104">Restaure toutes les fenêtres de bureau à l’État où elles se trouvaient avant la dernière commande [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="02262-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="02262-105">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner **Annuler réduire toutes les fenêtres** (sur les systèmes plus anciens) ou un second clic sur l’icône **afficher le bureau** dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="02262-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="02262-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02262-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="02262-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02262-107">Parameters</span></span>

<span data-ttu-id="02262-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="02262-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02262-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02262-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="02262-110">JScript</span><span class="sxs-lookup"><span data-stu-id="02262-110">JScript</span></span>

<span data-ttu-id="02262-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="02262-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="02262-112">VB</span><span class="sxs-lookup"><span data-stu-id="02262-112">VB</span></span>

<span data-ttu-id="02262-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="02262-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02262-114">Notes</span><span class="sxs-lookup"><span data-stu-id="02262-114">Remarks</span></span>

<span data-ttu-id="02262-115">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. UndoMinimizeAll**](./shell-undominimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="02262-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="02262-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="02262-116">Examples</span></span>

<span data-ttu-id="02262-117">Les exemples suivants illustrent l’utilisation de **UndoMinimizeALL** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="02262-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="02262-118">Langage</span><span class="sxs-lookup"><span data-stu-id="02262-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="02262-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="02262-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="02262-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="02262-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="02262-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="02262-121">Requirements</span></span>



| <span data-ttu-id="02262-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02262-122">Requirement</span></span> | <span data-ttu-id="02262-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="02262-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02262-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02262-124">Minimum supported client</span></span><br/> | <span data-ttu-id="02262-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02262-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="02262-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02262-126">Minimum supported server</span></span><br/> | <span data-ttu-id="02262-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02262-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02262-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="02262-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="02262-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02262-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="02262-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="02262-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02262-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02262-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="02262-132">DLL</span><span class="sxs-lookup"><span data-stu-id="02262-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02262-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="02262-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
