---
description: Mosaïque verticalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner les fenêtres de mosaïque verticalement.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Shell. TileVertically, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973675"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="95411-104">Shell. TileVertically, méthode</span><span class="sxs-lookup"><span data-stu-id="95411-104">Shell.TileVertically method</span></span>

<span data-ttu-id="95411-105">Mosaïque verticalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="95411-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="95411-106">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner les **fenêtres de mosaïque verticalement**.</span><span class="sxs-lookup"><span data-stu-id="95411-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="95411-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95411-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="95411-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95411-108">Parameters</span></span>

<span data-ttu-id="95411-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="95411-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="95411-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="95411-110">Examples</span></span>

<span data-ttu-id="95411-111">L’exemple suivant montre **TileVertically** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="95411-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="95411-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="95411-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="95411-113">Langage</span><span class="sxs-lookup"><span data-stu-id="95411-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="95411-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="95411-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="95411-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="95411-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="95411-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="95411-116">Requirements</span></span>



| <span data-ttu-id="95411-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95411-117">Requirement</span></span> | <span data-ttu-id="95411-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="95411-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95411-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95411-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95411-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95411-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95411-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95411-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95411-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95411-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95411-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="95411-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95411-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95411-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="95411-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="95411-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95411-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95411-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="95411-127">DLL</span><span class="sxs-lookup"><span data-stu-id="95411-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95411-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="95411-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




