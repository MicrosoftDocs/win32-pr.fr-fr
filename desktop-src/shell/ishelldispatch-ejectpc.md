---
description: Éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu Démarrer et à sélectionner éjecter le PC, si votre ordinateur prend en charge cette commande.
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
ms.openlocfilehash: d85dd8c007338dca3d68183bc9ba3fbd333195ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201712"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="c487e-104">Méthode IShellDispatch. EjectPC</span><span class="sxs-lookup"><span data-stu-id="c487e-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="c487e-105">Éjecte l’ordinateur de sa station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="c487e-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="c487e-106">Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **éjecter le PC**, si votre ordinateur prend en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="c487e-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="c487e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c487e-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="c487e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c487e-108">Parameters</span></span>

<span data-ttu-id="c487e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c487e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c487e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c487e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c487e-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c487e-111">JScript</span></span>

<span data-ttu-id="c487e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c487e-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c487e-113">VB</span><span class="sxs-lookup"><span data-stu-id="c487e-113">VB</span></span>

<span data-ttu-id="c487e-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c487e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c487e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c487e-115">Remarks</span></span>

<span data-ttu-id="c487e-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="c487e-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c487e-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c487e-117">Examples</span></span>

<span data-ttu-id="c487e-118">Les exemples suivants illustrent l’utilisation de **EjectPC** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c487e-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c487e-119">Langage</span><span class="sxs-lookup"><span data-stu-id="c487e-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="c487e-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="c487e-120">VBScript:</span></span>


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



<span data-ttu-id="c487e-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c487e-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c487e-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c487e-122">Requirements</span></span>



| <span data-ttu-id="c487e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c487e-123">Requirement</span></span> | <span data-ttu-id="c487e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c487e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c487e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c487e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c487e-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c487e-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c487e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c487e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c487e-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c487e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c487e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c487e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c487e-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c487e-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c487e-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="c487e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c487e-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c487e-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c487e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c487e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c487e-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c487e-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




