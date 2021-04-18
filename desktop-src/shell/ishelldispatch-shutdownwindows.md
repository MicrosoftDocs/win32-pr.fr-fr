---
description: Affiche la boîte de dialogue arrêter Windows. Cela revient à cliquer sur le menu Démarrer et à sélectionner arrêter.
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Méthode IShellDispatch. ShutdownWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c111e1b740857337953cdcdf81735a8c0568ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991144"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="8ff8f-104">Méthode IShellDispatch. ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="8ff8f-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="8ff8f-105">Affiche la boîte de dialogue **arrêter Windows** .</span><span class="sxs-lookup"><span data-stu-id="8ff8f-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="8ff8f-106">Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="8ff8f-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ff8f-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="8ff8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ff8f-108">Parameters</span></span>

<span data-ttu-id="8ff8f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8ff8f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ff8f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ff8f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8ff8f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="8ff8f-111">JScript</span></span>

<span data-ttu-id="8ff8f-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8ff8f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="8ff8f-113">VB</span><span class="sxs-lookup"><span data-stu-id="8ff8f-113">VB</span></span>

<span data-ttu-id="8ff8f-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8ff8f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff8f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8ff8f-115">Remarks</span></span>

<span data-ttu-id="8ff8f-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ShutdownWindows**](shell-shutdownwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="8ff8f-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="8ff8f-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="8ff8f-117">Examples</span></span>

<span data-ttu-id="8ff8f-118">L’exemple suivant illustre l’utilisation de **ShutdownWindows** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8ff8f-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8ff8f-119">Langage</span><span class="sxs-lookup"><span data-stu-id="8ff8f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="8ff8f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="8ff8f-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8ff8f-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8ff8f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8ff8f-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ff8f-122">Requirements</span></span>



| <span data-ttu-id="8ff8f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ff8f-123">Requirement</span></span> | <span data-ttu-id="8ff8f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ff8f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff8f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff8f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff8f-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ff8f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ff8f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff8f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff8f-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ff8f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ff8f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ff8f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff8f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff8f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8ff8f-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="8ff8f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ff8f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ff8f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8ff8f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff8f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff8f-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8ff8f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




