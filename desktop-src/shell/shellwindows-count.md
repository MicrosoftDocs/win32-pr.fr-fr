---
description: Contient le nombre d’éléments de la collection.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: ShellWindows. Count, propriété (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a8d5b9e605650ba7d3cb6036e8abfac58c0b8597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973730"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="604de-103">ShellWindows. Count (propriété)</span><span class="sxs-lookup"><span data-stu-id="604de-103">ShellWindows.Count property</span></span>

<span data-ttu-id="604de-104">Contient le nombre d’éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="604de-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="604de-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="604de-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="604de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="604de-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="604de-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="604de-107">Property value</span></span>

<span data-ttu-id="604de-108">**Entier** qui contient une valeur pour la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="604de-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="604de-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="604de-109">Examples</span></span>

<span data-ttu-id="604de-110">L’exemple suivant montre le **nombre** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="604de-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="604de-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="604de-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="604de-112">Langage</span><span class="sxs-lookup"><span data-stu-id="604de-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="604de-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="604de-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="604de-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="604de-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="604de-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="604de-115">Requirements</span></span>



| <span data-ttu-id="604de-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="604de-116">Requirement</span></span> | <span data-ttu-id="604de-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="604de-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="604de-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="604de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="604de-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="604de-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="604de-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="604de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="604de-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="604de-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="604de-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="604de-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="604de-123"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="604de-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="604de-124">DLL</span><span class="sxs-lookup"><span data-stu-id="604de-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="604de-125"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="604de-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




