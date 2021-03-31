---
description: Affiche le centre d’aide et de support Windows. Cette méthode a le même effet que le fait de cliquer sur le menu Démarrer et de sélectionner aide et support.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Shell. Help, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202904"
---
# <a name="shellhelp-method"></a><span data-ttu-id="03d33-104">Shell. Help, méthode</span><span class="sxs-lookup"><span data-stu-id="03d33-104">Shell.Help method</span></span>

<span data-ttu-id="03d33-105">Affiche le centre d’aide et de support Windows.</span><span class="sxs-lookup"><span data-stu-id="03d33-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="03d33-106">Cette méthode a le même effet que le fait de cliquer sur le menu **Démarrer** et de sélectionner **aide et support**.</span><span class="sxs-lookup"><span data-stu-id="03d33-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d33-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03d33-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="03d33-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03d33-108">Parameters</span></span>

<span data-ttu-id="03d33-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="03d33-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03d33-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03d33-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="03d33-111">JScript</span><span class="sxs-lookup"><span data-stu-id="03d33-111">JScript</span></span>

<span data-ttu-id="03d33-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03d33-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="03d33-113">VB</span><span class="sxs-lookup"><span data-stu-id="03d33-113">VB</span></span>

<span data-ttu-id="03d33-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03d33-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="03d33-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="03d33-115">Examples</span></span>

<span data-ttu-id="03d33-116">L’exemple suivant montre l' **aide** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="03d33-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="03d33-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="03d33-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="03d33-118">Langage</span><span class="sxs-lookup"><span data-stu-id="03d33-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="03d33-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="03d33-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="03d33-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="03d33-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="03d33-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="03d33-121">Requirements</span></span>



| <span data-ttu-id="03d33-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03d33-122">Requirement</span></span> | <span data-ttu-id="03d33-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="03d33-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d33-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03d33-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03d33-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03d33-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03d33-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03d33-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03d33-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03d33-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03d33-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="03d33-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d33-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d33-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="03d33-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="03d33-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03d33-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03d33-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="03d33-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03d33-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03d33-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="03d33-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




