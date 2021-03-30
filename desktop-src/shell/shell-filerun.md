---
description: Affiche la boîte de dialogue Exécuter à l’utilisateur. Cette méthode a le même effet que lorsque vous cliquez sur le menu Démarrer et sélectionnez Exécuter.
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: Shell. FileRun, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973699"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="5c05d-104">Shell. FileRun, méthode</span><span class="sxs-lookup"><span data-stu-id="5c05d-104">Shell.FileRun method</span></span>

<span data-ttu-id="5c05d-105">Affiche la boîte de dialogue **exécuter** à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c05d-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="5c05d-106">Cette méthode a le même effet que lorsque vous cliquez sur le menu **Démarrer** et sélectionnez **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="5c05d-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c05d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c05d-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="5c05d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c05d-108">Parameters</span></span>

<span data-ttu-id="5c05d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5c05d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c05d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c05d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5c05d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="5c05d-111">JScript</span></span>

<span data-ttu-id="5c05d-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5c05d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="5c05d-113">VB</span><span class="sxs-lookup"><span data-stu-id="5c05d-113">VB</span></span>

<span data-ttu-id="5c05d-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5c05d-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="5c05d-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="5c05d-115">Examples</span></span>

<span data-ttu-id="5c05d-116">L’exemple suivant montre **FileRun** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5c05d-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="5c05d-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c05d-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5c05d-118">Langage</span><span class="sxs-lookup"><span data-stu-id="5c05d-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="5c05d-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="5c05d-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5c05d-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="5c05d-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5c05d-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5c05d-121">Requirements</span></span>



| <span data-ttu-id="5c05d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c05d-122">Requirement</span></span> | <span data-ttu-id="5c05d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c05d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c05d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c05d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c05d-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c05d-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c05d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c05d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c05d-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c05d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5c05d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c05d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c05d-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c05d-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5c05d-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="5c05d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c05d-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c05d-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5c05d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5c05d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c05d-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5c05d-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




