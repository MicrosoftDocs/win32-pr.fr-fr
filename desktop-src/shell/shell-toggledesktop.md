---
description: 'Méthode Shell. ToggleDesktop : affiche ou masque le bureau.'
title: Shell. ToggleDesktop, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: c0d6c1e03db960c6abc8abc28ba8e79755fce639
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083677"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="02e0d-103">Shell. ToggleDesktop, méthode</span><span class="sxs-lookup"><span data-stu-id="02e0d-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="02e0d-104">Affiche ou masque le bureau.</span><span class="sxs-lookup"><span data-stu-id="02e0d-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02e0d-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="02e0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02e0d-106">Parameters</span></span>

<span data-ttu-id="02e0d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="02e0d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02e0d-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02e0d-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="02e0d-109">JScript</span><span class="sxs-lookup"><span data-stu-id="02e0d-109">JScript</span></span>

<span data-ttu-id="02e0d-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="02e0d-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="02e0d-111">VB</span><span class="sxs-lookup"><span data-stu-id="02e0d-111">VB</span></span>

<span data-ttu-id="02e0d-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="02e0d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e0d-113">Notes </span><span class="sxs-lookup"><span data-stu-id="02e0d-113">Remarks</span></span>

<span data-ttu-id="02e0d-114">Cette méthode a le même effet que le bouton **afficher le bureau** sur la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="02e0d-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="02e0d-115">Il masque toutes les fenêtres ouvertes pour afficher le bureau ou masque le bureau en affichant toutes les fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="02e0d-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="02e0d-116">La méthode **ToggleDesktop** n’affiche pas d’interface utilisateur, elle appelle simplement l’action bascule.</span><span class="sxs-lookup"><span data-stu-id="02e0d-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="02e0d-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="02e0d-117">Examples</span></span>

<span data-ttu-id="02e0d-118">Les exemples suivants illustrent l’utilisation correcte de **ToggleDesktop** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="02e0d-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="02e0d-119">Langage</span><span class="sxs-lookup"><span data-stu-id="02e0d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="02e0d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="02e0d-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="02e0d-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="02e0d-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="02e0d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02e0d-122">Requirements</span></span>



| <span data-ttu-id="02e0d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02e0d-123">Requirement</span></span> | <span data-ttu-id="02e0d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="02e0d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e0d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02e0d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="02e0d-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02e0d-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="02e0d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02e0d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="02e0d-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02e0d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="02e0d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="02e0d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e0d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e0d-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="02e0d-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="02e0d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02e0d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02e0d-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="02e0d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="02e0d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e0d-134"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="02e0d-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




