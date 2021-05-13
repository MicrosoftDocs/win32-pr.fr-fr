---
description: 'Méthode IShellDispatch4. WindowsSecurity : affiche la boîte de dialogue sécurité Windows.'
title: Méthode IShellDispatch4. WindowsSecurity (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 6eadb580c73e5e56592c94e997bdc22c2cf894b4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843020"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="f2bfa-103">Méthode IShellDispatch4. WindowsSecurity</span><span class="sxs-lookup"><span data-stu-id="f2bfa-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="f2bfa-104">Affiche la boîte de dialogue **sécurité Windows** .</span><span class="sxs-lookup"><span data-stu-id="f2bfa-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bfa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2bfa-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="f2bfa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2bfa-106">Parameters</span></span>

<span data-ttu-id="f2bfa-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2bfa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2bfa-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f2bfa-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f2bfa-109">JScript</span><span class="sxs-lookup"><span data-stu-id="f2bfa-109">JScript</span></span>

<span data-ttu-id="f2bfa-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f2bfa-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f2bfa-111">VB</span><span class="sxs-lookup"><span data-stu-id="f2bfa-111">VB</span></span>

<span data-ttu-id="f2bfa-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f2bfa-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2bfa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f2bfa-113">Remarks</span></span>

<span data-ttu-id="f2bfa-114">Cette méthode affiche la boîte de dialogue qui s’affiche après avoir appuyé sur CTRL + ALT + SUPPR ou à l’aide de l’option sécurité dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="f2bfa-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="f2bfa-115">Cette méthode peut être utilisée uniquement lorsqu’elle est connectée par une session terminal à Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="f2bfa-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f2bfa-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="f2bfa-116">Examples</span></span>

<span data-ttu-id="f2bfa-117">Les exemples suivants illustrent l’utilisation de **WindowsSecurity** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f2bfa-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f2bfa-118">Langage</span><span class="sxs-lookup"><span data-stu-id="f2bfa-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="f2bfa-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="f2bfa-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f2bfa-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="f2bfa-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f2bfa-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f2bfa-121">Requirements</span></span>



| <span data-ttu-id="f2bfa-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2bfa-122">Requirement</span></span> | <span data-ttu-id="f2bfa-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2bfa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bfa-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2bfa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bfa-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2bfa-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="f2bfa-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2bfa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bfa-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2bfa-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f2bfa-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2bfa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2bfa-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2bfa-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f2bfa-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="f2bfa-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2bfa-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2bfa-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f2bfa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f2bfa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2bfa-133"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="f2bfa-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




