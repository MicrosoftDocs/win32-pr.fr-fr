---
description: Shell. ShutdownWindows, méthode-affiche la boîte de dialogue arrêt de Windows. Cela revient à cliquer sur le menu Démarrer et à sélectionner arrêter.
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
ms.openlocfilehash: 2a3c0746caccb360f6f7f0156b72a57ed0a2d2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083667"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="8e5d3-104">Shell. ShutdownWindows, méthode</span><span class="sxs-lookup"><span data-stu-id="8e5d3-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="8e5d3-105">Affiche la boîte de dialogue **arrêter Windows** .</span><span class="sxs-lookup"><span data-stu-id="8e5d3-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="8e5d3-106">Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="8e5d3-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e5d3-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="8e5d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e5d3-108">Parameters</span></span>

<span data-ttu-id="8e5d3-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8e5d3-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="8e5d3-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="8e5d3-110">Examples</span></span>

<span data-ttu-id="8e5d3-111">L’exemple suivant montre **ShutdownWindows** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8e5d3-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="8e5d3-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8e5d3-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8e5d3-113">Langage</span><span class="sxs-lookup"><span data-stu-id="8e5d3-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="8e5d3-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="8e5d3-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="8e5d3-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8e5d3-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8e5d3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e5d3-116">Requirements</span></span>



| <span data-ttu-id="8e5d3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e5d3-117">Requirement</span></span> | <span data-ttu-id="8e5d3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e5d3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5d3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e5d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5d3-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e5d3-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e5d3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e5d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5d3-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e5d3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e5d3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e5d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e5d3-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5d3-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8e5d3-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="8e5d3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e5d3-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e5d3-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8e5d3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8e5d3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e5d3-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8e5d3-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




