---
description: Cascade toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des fenêtres en cascade.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Shell. CascadeWindows, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529416"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="c550e-104">Shell. CascadeWindows, méthode</span><span class="sxs-lookup"><span data-stu-id="c550e-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="c550e-105">Cascade toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="c550e-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="c550e-106">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des **fenêtres en cascade**.</span><span class="sxs-lookup"><span data-stu-id="c550e-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c550e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c550e-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="c550e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c550e-108">Parameters</span></span>

<span data-ttu-id="c550e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c550e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c550e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c550e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c550e-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c550e-111">JScript</span></span>

<span data-ttu-id="c550e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c550e-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c550e-113">VB</span><span class="sxs-lookup"><span data-stu-id="c550e-113">VB</span></span>

<span data-ttu-id="c550e-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c550e-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c550e-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="c550e-115">Examples</span></span>

<span data-ttu-id="c550e-116">L’exemple suivant montre **CascadeWindows** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c550e-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="c550e-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c550e-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c550e-118">Langage</span><span class="sxs-lookup"><span data-stu-id="c550e-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="c550e-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="c550e-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c550e-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c550e-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c550e-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c550e-121">Requirements</span></span>



| <span data-ttu-id="c550e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c550e-122">Requirement</span></span> | <span data-ttu-id="c550e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c550e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c550e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c550e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c550e-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c550e-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c550e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c550e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c550e-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c550e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c550e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c550e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c550e-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c550e-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c550e-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="c550e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c550e-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c550e-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c550e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c550e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c550e-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c550e-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




