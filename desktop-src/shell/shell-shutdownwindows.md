---
description: Affiche la boîte de dialogue arrêter Windows. Cela revient à cliquer sur le menu Démarrer et à sélectionner arrêter.
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Shell. ShutdownWindows, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 804a1e211e191206d20f83d85dee2202492bfd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203436"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="77001-104">Shell. ShutdownWindows, méthode</span><span class="sxs-lookup"><span data-stu-id="77001-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="77001-105">Affiche la boîte de dialogue **arrêter Windows** .</span><span class="sxs-lookup"><span data-stu-id="77001-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="77001-106">Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="77001-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="77001-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77001-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="77001-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77001-108">Parameters</span></span>

<span data-ttu-id="77001-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="77001-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="77001-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="77001-110">Examples</span></span>

<span data-ttu-id="77001-111">L’exemple suivant montre **ShutdownWindows** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="77001-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="77001-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="77001-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="77001-113">Langage</span><span class="sxs-lookup"><span data-stu-id="77001-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="77001-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="77001-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="77001-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="77001-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="77001-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77001-116">Requirements</span></span>



| <span data-ttu-id="77001-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77001-117">Requirement</span></span> | <span data-ttu-id="77001-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="77001-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77001-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77001-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77001-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77001-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="77001-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77001-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77001-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77001-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="77001-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="77001-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77001-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77001-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="77001-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="77001-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77001-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77001-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="77001-127">DLL</span><span class="sxs-lookup"><span data-stu-id="77001-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77001-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="77001-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




