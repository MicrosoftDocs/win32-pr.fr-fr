---
description: Crée et retourne un objet ShellWindows. Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.
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
ms.openlocfilehash: cb5f84caebf38deb27c7fb60565167793fead561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753077"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="0740b-104">IShellDispatch. Windows, méthode</span><span class="sxs-lookup"><span data-stu-id="0740b-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="0740b-105">Crée et retourne un objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="0740b-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="0740b-106">Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="0740b-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="0740b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0740b-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="0740b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0740b-108">Parameters</span></span>

<span data-ttu-id="0740b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0740b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0740b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0740b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0740b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="0740b-111">JScript</span></span>

<span data-ttu-id="0740b-112">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="0740b-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="0740b-113">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="0740b-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="0740b-114">VB</span><span class="sxs-lookup"><span data-stu-id="0740b-114">VB</span></span>

<span data-ttu-id="0740b-115">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="0740b-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="0740b-116">Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="0740b-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0740b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0740b-117">Remarks</span></span>

<span data-ttu-id="0740b-118">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Windows**](shell-windows.md) .</span><span class="sxs-lookup"><span data-stu-id="0740b-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0740b-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="0740b-119">Examples</span></span>

<span data-ttu-id="0740b-120">Les exemples suivants utilisent **Windows** pour récupérer l’objet [**ShellWindows**](shellwindows.md) et afficher le nombre d’éléments qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="0740b-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="0740b-121">L’utilisation est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0740b-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0740b-122">Langage</span><span class="sxs-lookup"><span data-stu-id="0740b-122">JScript:</span></span>


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



<span data-ttu-id="0740b-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="0740b-123">VBScript:</span></span>


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



<span data-ttu-id="0740b-124">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="0740b-124">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0740b-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0740b-125">Requirements</span></span>



| <span data-ttu-id="0740b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0740b-126">Requirement</span></span> | <span data-ttu-id="0740b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0740b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0740b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0740b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0740b-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0740b-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0740b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0740b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0740b-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0740b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0740b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0740b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0740b-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0740b-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0740b-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="0740b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0740b-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0740b-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0740b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0740b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0740b-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="0740b-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
