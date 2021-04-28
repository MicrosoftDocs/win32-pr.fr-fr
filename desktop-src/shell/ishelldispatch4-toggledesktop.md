---
description: 'Méthode IShellDispatch4. ToggleDesktop : affiche ou masque le bureau.'
title: Méthode IShellDispatch4. ToggleDesktop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: b635408ed8a44b8bb0d27e52c167470f80f61b18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116817"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="1d049-103">Méthode IShellDispatch4. ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="1d049-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="1d049-104">Affiche ou masque le bureau.</span><span class="sxs-lookup"><span data-stu-id="1d049-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d049-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d049-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="1d049-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d049-106">Parameters</span></span>

<span data-ttu-id="1d049-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d049-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d049-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1d049-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1d049-109">JScript</span><span class="sxs-lookup"><span data-stu-id="1d049-109">JScript</span></span>

<span data-ttu-id="1d049-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1d049-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1d049-111">VB</span><span class="sxs-lookup"><span data-stu-id="1d049-111">VB</span></span>

<span data-ttu-id="1d049-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1d049-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d049-113">Notes </span><span class="sxs-lookup"><span data-stu-id="1d049-113">Remarks</span></span>

<span data-ttu-id="1d049-114">Cette méthode a le même effet que le bouton **afficher le bureau** sur la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="1d049-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="1d049-115">Il masque toutes les fenêtres ouvertes pour afficher le bureau ou masque le bureau en affichant toutes les fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="1d049-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="1d049-116">La méthode **ToggleDesktop** n’affiche pas d’interface utilisateur, elle appelle simplement l’action bascule.</span><span class="sxs-lookup"><span data-stu-id="1d049-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="1d049-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="1d049-117">Examples</span></span>

<span data-ttu-id="1d049-118">Les exemples suivants illustrent l’utilisation correcte de **ToggleDesktop** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d049-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1d049-119">Langage</span><span class="sxs-lookup"><span data-stu-id="1d049-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="1d049-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="1d049-120">VBScript:</span></span>


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



<span data-ttu-id="1d049-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="1d049-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1d049-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d049-122">Requirements</span></span>



| <span data-ttu-id="1d049-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d049-123">Requirement</span></span> | <span data-ttu-id="1d049-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d049-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d049-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d049-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1d049-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d049-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1d049-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d049-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1d049-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d049-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1d049-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d049-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d049-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d049-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1d049-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="1d049-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d049-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d049-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1d049-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1d049-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d049-134"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1d049-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




