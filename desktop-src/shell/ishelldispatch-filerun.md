---
description: Affiche la boîte de dialogue Exécuter à l’utilisateur.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Méthode IShellDispatch. FileRun (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753093"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="df1ca-103">Méthode IShellDispatch. FileRun</span><span class="sxs-lookup"><span data-stu-id="df1ca-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="df1ca-104">Affiche la boîte de dialogue **exécuter** à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df1ca-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df1ca-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="df1ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df1ca-106">Parameters</span></span>

<span data-ttu-id="df1ca-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="df1ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df1ca-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df1ca-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="df1ca-109">JScript</span><span class="sxs-lookup"><span data-stu-id="df1ca-109">JScript</span></span>

<span data-ttu-id="df1ca-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="df1ca-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="df1ca-111">VB</span><span class="sxs-lookup"><span data-stu-id="df1ca-111">VB</span></span>

<span data-ttu-id="df1ca-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="df1ca-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1ca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="df1ca-113">Remarks</span></span>

<span data-ttu-id="df1ca-114">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FileRun**](shell-filerun.md) .</span><span class="sxs-lookup"><span data-stu-id="df1ca-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="df1ca-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="df1ca-115">Examples</span></span>

<span data-ttu-id="df1ca-116">Les exemples suivants illustrent l’utilisation de **FileRun** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="df1ca-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="df1ca-117">Langage</span><span class="sxs-lookup"><span data-stu-id="df1ca-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="df1ca-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="df1ca-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="df1ca-119">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="df1ca-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="df1ca-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="df1ca-120">Requirements</span></span>



| <span data-ttu-id="df1ca-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df1ca-121">Requirement</span></span> | <span data-ttu-id="df1ca-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="df1ca-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df1ca-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df1ca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df1ca-124">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df1ca-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="df1ca-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df1ca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df1ca-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df1ca-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df1ca-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="df1ca-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="df1ca-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="df1ca-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="df1ca-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="df1ca-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df1ca-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df1ca-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="df1ca-131">DLL</span><span class="sxs-lookup"><span data-stu-id="df1ca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df1ca-132"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="df1ca-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




