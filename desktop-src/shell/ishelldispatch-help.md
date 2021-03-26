---
description: Affiche la fenêtre aide et support Windows. Cette méthode a le même effet que le fait de cliquer sur le menu Démarrer et de sélectionner aide et support.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: IShellDispatch. Help, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972422"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="dcc14-104">IShellDispatch. Help, méthode</span><span class="sxs-lookup"><span data-stu-id="dcc14-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="dcc14-105">Affiche la fenêtre aide et support Windows.</span><span class="sxs-lookup"><span data-stu-id="dcc14-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="dcc14-106">Cette méthode a le même effet que le fait de cliquer sur le menu **Démarrer** et de sélectionner **aide et support**.</span><span class="sxs-lookup"><span data-stu-id="dcc14-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc14-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcc14-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="dcc14-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcc14-108">Parameters</span></span>

<span data-ttu-id="dcc14-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dcc14-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcc14-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcc14-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="dcc14-111">JScript</span><span class="sxs-lookup"><span data-stu-id="dcc14-111">JScript</span></span>

<span data-ttu-id="dcc14-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dcc14-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="dcc14-113">VB</span><span class="sxs-lookup"><span data-stu-id="dcc14-113">VB</span></span>

<span data-ttu-id="dcc14-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dcc14-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc14-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dcc14-115">Remarks</span></span>

<span data-ttu-id="dcc14-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Help**](shell-help.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc14-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="dcc14-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="dcc14-117">Examples</span></span>

<span data-ttu-id="dcc14-118">Les exemples suivants illustrent l’utilisation de l' **aide** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dcc14-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dcc14-119">Langage</span><span class="sxs-lookup"><span data-stu-id="dcc14-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="dcc14-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="dcc14-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="dcc14-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="dcc14-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dcc14-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dcc14-122">Requirements</span></span>



| <span data-ttu-id="dcc14-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcc14-123">Requirement</span></span> | <span data-ttu-id="dcc14-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcc14-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc14-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc14-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc14-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcc14-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dcc14-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc14-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc14-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcc14-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dcc14-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcc14-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc14-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc14-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dcc14-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="dcc14-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcc14-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcc14-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dcc14-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc14-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc14-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc14-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




