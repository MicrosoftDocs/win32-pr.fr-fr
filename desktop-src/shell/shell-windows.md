---
description: Crée et retourne un objet ShellWindows. Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.
title: Shell. Windows, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: a865109f926253215e5ad39227cfe3d480e9ccc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952834"
---
# <a name="shellwindows-method"></a><span data-ttu-id="604bb-104">Shell. Windows, méthode</span><span class="sxs-lookup"><span data-stu-id="604bb-104">Shell.Windows method</span></span>

<span data-ttu-id="604bb-105">Crée et retourne un objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="604bb-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="604bb-106">Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="604bb-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="604bb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="604bb-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="604bb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="604bb-108">Parameters</span></span>

<span data-ttu-id="604bb-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="604bb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="604bb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="604bb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="604bb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="604bb-111">JScript</span></span>

<span data-ttu-id="604bb-112">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="604bb-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="604bb-113">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="604bb-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="604bb-114">VB</span><span class="sxs-lookup"><span data-stu-id="604bb-114">VB</span></span>

<span data-ttu-id="604bb-115">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="604bb-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="604bb-116">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="604bb-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="604bb-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="604bb-117">Examples</span></span>

<span data-ttu-id="604bb-118">L’exemple suivant utilise **Windows** pour récupérer l’objet [**ShellWindows**](shellwindows.md) et afficher le nombre d’éléments qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="604bb-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="604bb-119">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="604bb-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="604bb-120">Langage</span><span class="sxs-lookup"><span data-stu-id="604bb-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="604bb-121">VBScript</span><span class="sxs-lookup"><span data-stu-id="604bb-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="604bb-122">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="604bb-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="604bb-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="604bb-123">Requirements</span></span>



| <span data-ttu-id="604bb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="604bb-124">Requirement</span></span> | <span data-ttu-id="604bb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="604bb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="604bb-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="604bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="604bb-127">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="604bb-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="604bb-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="604bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="604bb-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="604bb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="604bb-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="604bb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="604bb-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="604bb-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="604bb-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="604bb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="604bb-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="604bb-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="604bb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="604bb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="604bb-135"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="604bb-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
