---
description: 'Méthode IShellDispatch. Windows : crée et retourne un objet ShellWindows. Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.'
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Méthode IShellDispatch. Windows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117167"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="a0265-104">IShellDispatch. Windows, méthode</span><span class="sxs-lookup"><span data-stu-id="a0265-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="a0265-105">Crée et retourne un objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="a0265-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="a0265-106">Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="a0265-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0265-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0265-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="a0265-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0265-108">Parameters</span></span>

<span data-ttu-id="a0265-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a0265-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0265-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a0265-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a0265-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a0265-111">JScript</span></span>

<span data-ttu-id="a0265-112">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="a0265-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="a0265-113">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="a0265-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="a0265-114">VB</span><span class="sxs-lookup"><span data-stu-id="a0265-114">VB</span></span>

<span data-ttu-id="a0265-115">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="a0265-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="a0265-116">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="a0265-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0265-117">Notes </span><span class="sxs-lookup"><span data-stu-id="a0265-117">Remarks</span></span>

<span data-ttu-id="a0265-118">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Windows**](shell-windows.md) .</span><span class="sxs-lookup"><span data-stu-id="a0265-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a0265-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="a0265-119">Examples</span></span>

<span data-ttu-id="a0265-120">Les exemples suivants utilisent **Windows** pour récupérer l’objet [**ShellWindows**](shellwindows.md) et afficher le nombre d’éléments qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="a0265-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="a0265-121">L’utilisation est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a0265-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a0265-122">Langage</span><span class="sxs-lookup"><span data-stu-id="a0265-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="a0265-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="a0265-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a0265-124">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="a0265-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a0265-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0265-125">Requirements</span></span>



| <span data-ttu-id="a0265-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0265-126">Requirement</span></span> | <span data-ttu-id="a0265-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0265-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0265-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0265-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0265-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0265-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0265-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0265-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0265-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0265-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0265-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0265-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0265-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0265-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a0265-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="a0265-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0265-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0265-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a0265-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0265-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0265-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="a0265-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
