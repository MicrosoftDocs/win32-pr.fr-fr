---
description: Affiche la boîte de dialogue date et heure. Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner ajuster la date/l’heure.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: IShellDispatch. SetTime, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863142"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="7109e-104">IShellDispatch. SetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="7109e-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="7109e-105">Affiche la boîte de dialogue **date et heure** .</span><span class="sxs-lookup"><span data-stu-id="7109e-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="7109e-106">Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner **ajuster la date/l’heure**.</span><span class="sxs-lookup"><span data-stu-id="7109e-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7109e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7109e-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="7109e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7109e-108">Parameters</span></span>

<span data-ttu-id="7109e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7109e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7109e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7109e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7109e-111">JScript</span><span class="sxs-lookup"><span data-stu-id="7109e-111">JScript</span></span>

<span data-ttu-id="7109e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7109e-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7109e-113">VB</span><span class="sxs-lookup"><span data-stu-id="7109e-113">VB</span></span>

<span data-ttu-id="7109e-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7109e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7109e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7109e-115">Remarks</span></span>

<span data-ttu-id="7109e-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. SetTime**](shell-settime.md) .</span><span class="sxs-lookup"><span data-stu-id="7109e-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7109e-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7109e-117">Examples</span></span>

<span data-ttu-id="7109e-118">Les exemples suivants illustrent l’utilisation de **setTime** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7109e-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7109e-119">Langage</span><span class="sxs-lookup"><span data-stu-id="7109e-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="7109e-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="7109e-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="7109e-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7109e-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="7109e-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7109e-122">Requirements</span></span>



| <span data-ttu-id="7109e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7109e-123">Requirement</span></span> | <span data-ttu-id="7109e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7109e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7109e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7109e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7109e-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7109e-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7109e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7109e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7109e-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7109e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7109e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7109e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7109e-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7109e-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7109e-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="7109e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7109e-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7109e-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7109e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7109e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7109e-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="7109e-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




