---
description: 'Shell. Windows, méthode : crée et retourne un objet ShellWindows. Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.'
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
ms.openlocfilehash: d46e27781dc569b473615926509f51ed9d089af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104067"
---
# <a name="shellwindows-method"></a><span data-ttu-id="5295d-104">Shell. Windows, méthode</span><span class="sxs-lookup"><span data-stu-id="5295d-104">Shell.Windows method</span></span>

<span data-ttu-id="5295d-105">Crée et retourne un objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="5295d-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="5295d-106">Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="5295d-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="5295d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5295d-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="5295d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5295d-108">Parameters</span></span>

<span data-ttu-id="5295d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5295d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5295d-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5295d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5295d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="5295d-111">JScript</span></span>

<span data-ttu-id="5295d-112">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="5295d-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="5295d-113">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="5295d-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="5295d-114">VB</span><span class="sxs-lookup"><span data-stu-id="5295d-114">VB</span></span>

<span data-ttu-id="5295d-115">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="5295d-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="5295d-116">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="5295d-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="5295d-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="5295d-117">Examples</span></span>

<span data-ttu-id="5295d-118">L’exemple suivant utilise **Windows** pour récupérer l’objet [**ShellWindows**](shellwindows.md) et afficher le nombre d’éléments qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="5295d-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="5295d-119">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5295d-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5295d-120">Langage</span><span class="sxs-lookup"><span data-stu-id="5295d-120">JScript:</span></span>


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



<span data-ttu-id="5295d-121">VBScript</span><span class="sxs-lookup"><span data-stu-id="5295d-121">VBScript:</span></span>


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



<span data-ttu-id="5295d-122">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="5295d-122">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5295d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5295d-123">Requirements</span></span>



| <span data-ttu-id="5295d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5295d-124">Requirement</span></span> | <span data-ttu-id="5295d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5295d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5295d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5295d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5295d-127">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5295d-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5295d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5295d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5295d-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5295d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5295d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5295d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5295d-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5295d-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5295d-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="5295d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5295d-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5295d-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5295d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5295d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5295d-135"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5295d-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
