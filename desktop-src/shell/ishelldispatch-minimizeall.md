---
description: Réduit toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner réduire toutes les fenêtres sur les anciens systèmes ou cliquer sur l’icône Afficher le bureau dans la barre des tâches.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Méthode IShellDispatch. MinimizeAll (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527340"
---
# <a name="ishelldispatchminimizeall-method"></a><span data-ttu-id="a65d9-104">Méthode IShellDispatch. MinimizeAll</span><span class="sxs-lookup"><span data-stu-id="a65d9-104">IShellDispatch.MinimizeAll method</span></span>

<span data-ttu-id="a65d9-105">Réduit toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="a65d9-105">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="a65d9-106">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner **réduire toutes les fenêtres** sur les anciens systèmes ou cliquer sur l’icône **afficher le bureau** dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a65d9-106">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon on the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a65d9-107">Syntax</span></span>


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a><span data-ttu-id="a65d9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a65d9-108">Parameters</span></span>

<span data-ttu-id="a65d9-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a65d9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a65d9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a65d9-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a65d9-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a65d9-111">JScript</span></span>

<span data-ttu-id="a65d9-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a65d9-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a65d9-113">VB</span><span class="sxs-lookup"><span data-stu-id="a65d9-113">VB</span></span>

<span data-ttu-id="a65d9-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a65d9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a65d9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a65d9-115">Remarks</span></span>

<span data-ttu-id="a65d9-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="a65d9-116">This method is implemented and accessed through the [**Shell.MinimizeAll**](shell-minimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a65d9-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="a65d9-117">Examples</span></span>

<span data-ttu-id="a65d9-118">Les exemples suivants illustrent l’utilisation de **MinimizeAll** en cours d’utilisation pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a65d9-118">The following examples show the use of **MinimizeAll** in use for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a65d9-119">Langage</span><span class="sxs-lookup"><span data-stu-id="a65d9-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="a65d9-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="a65d9-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a65d9-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="a65d9-121">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a65d9-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a65d9-122">Requirements</span></span>



| <span data-ttu-id="a65d9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a65d9-123">Requirement</span></span> | <span data-ttu-id="a65d9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a65d9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65d9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a65d9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a65d9-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a65d9-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a65d9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a65d9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a65d9-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a65d9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a65d9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a65d9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65d9-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65d9-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a65d9-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="a65d9-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a65d9-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a65d9-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a65d9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a65d9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a65d9-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="a65d9-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a65d9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a65d9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65d9-136">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="a65d9-136">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="a65d9-137">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="a65d9-137">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




