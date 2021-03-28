---
description: 'Affiche la boîte de dialogue résultats de la recherche : ordinateurs. La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Méthode IShellDispatch. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972427"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="95250-104">Méthode IShellDispatch. FindComputer</span><span class="sxs-lookup"><span data-stu-id="95250-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="95250-105">Affiche la boîte de dialogue résultats de la **recherche : ordinateurs** .</span><span class="sxs-lookup"><span data-stu-id="95250-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="95250-106">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="95250-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="95250-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95250-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="95250-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95250-108">Parameters</span></span>

<span data-ttu-id="95250-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="95250-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95250-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95250-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="95250-111">JScript</span><span class="sxs-lookup"><span data-stu-id="95250-111">JScript</span></span>

<span data-ttu-id="95250-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="95250-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="95250-113">VB</span><span class="sxs-lookup"><span data-stu-id="95250-113">VB</span></span>

<span data-ttu-id="95250-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="95250-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95250-115">Notes</span><span class="sxs-lookup"><span data-stu-id="95250-115">Remarks</span></span>

<span data-ttu-id="95250-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FindComputer**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="95250-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="95250-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="95250-117">Examples</span></span>

<span data-ttu-id="95250-118">Les exemples suivants illustrent l’utilisation de **FindComputer** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="95250-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="95250-119">Langage</span><span class="sxs-lookup"><span data-stu-id="95250-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="95250-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="95250-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="95250-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="95250-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="95250-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="95250-122">Requirements</span></span>



| <span data-ttu-id="95250-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95250-123">Requirement</span></span> | <span data-ttu-id="95250-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="95250-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95250-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95250-125">Minimum supported client</span></span><br/> | <span data-ttu-id="95250-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95250-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95250-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95250-127">Minimum supported server</span></span><br/> | <span data-ttu-id="95250-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95250-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95250-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="95250-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="95250-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95250-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="95250-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="95250-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95250-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95250-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="95250-133">DLL</span><span class="sxs-lookup"><span data-stu-id="95250-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95250-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="95250-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




