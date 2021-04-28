---
description: 'Méthode IShellDispatch. EjectPC : éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu Démarrer et à sélectionner éjecter le PC, si votre ordinateur prend en charge cette commande.'
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Méthode IShellDispatch. EjectPC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac42e1a4331a553a03bac3da50a187e06c90859c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086637"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="5fd59-104">Méthode IShellDispatch. EjectPC</span><span class="sxs-lookup"><span data-stu-id="5fd59-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="5fd59-105">Éjecte l’ordinateur de sa station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="5fd59-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="5fd59-106">Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **éjecter le PC**, si votre ordinateur prend en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="5fd59-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd59-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fd59-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="5fd59-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fd59-108">Parameters</span></span>

<span data-ttu-id="5fd59-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5fd59-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fd59-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5fd59-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5fd59-111">JScript</span><span class="sxs-lookup"><span data-stu-id="5fd59-111">JScript</span></span>

<span data-ttu-id="5fd59-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5fd59-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="5fd59-113">VB</span><span class="sxs-lookup"><span data-stu-id="5fd59-113">VB</span></span>

<span data-ttu-id="5fd59-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5fd59-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd59-115">Notes </span><span class="sxs-lookup"><span data-stu-id="5fd59-115">Remarks</span></span>

<span data-ttu-id="5fd59-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd59-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="5fd59-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="5fd59-117">Examples</span></span>

<span data-ttu-id="5fd59-118">Les exemples suivants illustrent l’utilisation de **EjectPC** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5fd59-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5fd59-119">Langage</span><span class="sxs-lookup"><span data-stu-id="5fd59-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="5fd59-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="5fd59-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5fd59-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="5fd59-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5fd59-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fd59-122">Requirements</span></span>



| <span data-ttu-id="5fd59-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fd59-123">Requirement</span></span> | <span data-ttu-id="5fd59-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fd59-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd59-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fd59-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd59-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fd59-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5fd59-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fd59-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd59-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fd59-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5fd59-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fd59-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd59-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd59-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5fd59-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="5fd59-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5fd59-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5fd59-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5fd59-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd59-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd59-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd59-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




