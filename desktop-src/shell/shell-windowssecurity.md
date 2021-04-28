---
description: Shell. WindowsSecurity, méthode-affiche la boîte de dialogue sécurité Windows.
title: Shell. WindowsSecurity, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 94916E29-5960-4010-B2C6-0FAA1E4BF72D
ms.openlocfilehash: 7e04cc6d3a1a25f459da9f533fc562b1fc9d0b06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083597"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="47edb-103">Shell. WindowsSecurity, méthode</span><span class="sxs-lookup"><span data-stu-id="47edb-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="47edb-104">Affiche la boîte de dialogue **sécurité Windows** .</span><span class="sxs-lookup"><span data-stu-id="47edb-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="47edb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47edb-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="47edb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47edb-106">Parameters</span></span>

<span data-ttu-id="47edb-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="47edb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47edb-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="47edb-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="47edb-109">JScript</span><span class="sxs-lookup"><span data-stu-id="47edb-109">JScript</span></span>

<span data-ttu-id="47edb-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="47edb-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="47edb-111">VB</span><span class="sxs-lookup"><span data-stu-id="47edb-111">VB</span></span>

<span data-ttu-id="47edb-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="47edb-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47edb-113">Notes </span><span class="sxs-lookup"><span data-stu-id="47edb-113">Remarks</span></span>

<span data-ttu-id="47edb-114">Cette méthode affiche la boîte de dialogue qui s’affiche après avoir appuyé sur CTRL + ALT + SUPPR ou à l’aide de l’option sécurité dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="47edb-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="47edb-115">Cette méthode peut être utilisée uniquement lorsqu’elle est connectée par une session terminal à Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="47edb-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="47edb-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="47edb-116">Examples</span></span>

<span data-ttu-id="47edb-117">Les exemples suivants illustrent l’utilisation de **WindowsSecurity** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="47edb-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="47edb-118">Langage</span><span class="sxs-lookup"><span data-stu-id="47edb-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="47edb-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="47edb-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="47edb-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="47edb-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="47edb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47edb-121">Requirements</span></span>



| <span data-ttu-id="47edb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47edb-122">Requirement</span></span> | <span data-ttu-id="47edb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="47edb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47edb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47edb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="47edb-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47edb-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="47edb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47edb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="47edb-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47edb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="47edb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="47edb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="47edb-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47edb-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="47edb-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="47edb-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47edb-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47edb-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="47edb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="47edb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47edb-133"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="47edb-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




