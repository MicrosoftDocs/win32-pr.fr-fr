---
description: Mosaïques horizontalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection horizontale des fenêtres de mosaïque.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Shell. TileHorizontally, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203434"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="3b136-104">Shell. TileHorizontally, méthode</span><span class="sxs-lookup"><span data-stu-id="3b136-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="3b136-105">Mosaïques horizontalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="3b136-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="3b136-106">Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection **horizontale des fenêtres de mosaïque**.</span><span class="sxs-lookup"><span data-stu-id="3b136-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b136-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b136-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="3b136-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b136-108">Parameters</span></span>

<span data-ttu-id="3b136-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3b136-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="3b136-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="3b136-110">Examples</span></span>

<span data-ttu-id="3b136-111">L’exemple suivant montre **TileHorizontally** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3b136-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="3b136-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3b136-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3b136-113">Langage</span><span class="sxs-lookup"><span data-stu-id="3b136-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="3b136-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="3b136-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3b136-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="3b136-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3b136-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b136-116">Requirements</span></span>



| <span data-ttu-id="3b136-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b136-117">Requirement</span></span> | <span data-ttu-id="3b136-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b136-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b136-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b136-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3b136-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b136-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3b136-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b136-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3b136-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b136-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b136-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b136-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b136-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b136-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3b136-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="3b136-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b136-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b136-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3b136-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3b136-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b136-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3b136-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




