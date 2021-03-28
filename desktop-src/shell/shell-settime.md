---
description: Affiche la boîte de dialogue Propriétés de date et heure. Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner ajuster la date/l’heure.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Shell. SetTime, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973254"
---
# <a name="shellsettime-method"></a><span data-ttu-id="7ecf3-104">Shell. SetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="7ecf3-104">Shell.SetTime method</span></span>

<span data-ttu-id="7ecf3-105">Affiche la boîte de dialogue **Propriétés de date et heure** .</span><span class="sxs-lookup"><span data-stu-id="7ecf3-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="7ecf3-106">Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner **ajuster la date/l’heure**.</span><span class="sxs-lookup"><span data-stu-id="7ecf3-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ecf3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ecf3-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="7ecf3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ecf3-108">Parameters</span></span>

<span data-ttu-id="7ecf3-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7ecf3-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="7ecf3-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="7ecf3-110">Examples</span></span>

<span data-ttu-id="7ecf3-111">L’exemple suivant illustre la commande **setTime** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7ecf3-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="7ecf3-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7ecf3-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7ecf3-113">Langage</span><span class="sxs-lookup"><span data-stu-id="7ecf3-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="7ecf3-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="7ecf3-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7ecf3-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7ecf3-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7ecf3-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ecf3-116">Requirements</span></span>



| <span data-ttu-id="7ecf3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ecf3-117">Requirement</span></span> | <span data-ttu-id="7ecf3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ecf3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecf3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ecf3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ecf3-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ecf3-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ecf3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ecf3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ecf3-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ecf3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ecf3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ecf3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ecf3-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ecf3-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7ecf3-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="7ecf3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ecf3-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ecf3-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7ecf3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ecf3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ecf3-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="7ecf3-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




