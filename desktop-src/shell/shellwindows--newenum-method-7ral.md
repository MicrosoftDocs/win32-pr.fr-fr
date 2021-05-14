---
description: Crée et retourne un nouvel objet ShellWindows qui est une copie de cet objet ShellWindows.
title: Méthode ShellWindows._NewEnum (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: 944da80196db12d0bfa5d64767c5e6c2e8ff733e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841250"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="38773-103">ShellWindows. \_ NewEnum, méthode</span><span class="sxs-lookup"><span data-stu-id="38773-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="38773-104">Crée et retourne un nouvel objet [**ShellWindows**](shellwindows.md) qui est une copie de cet objet **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="38773-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="38773-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38773-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="38773-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38773-106">Parameters</span></span>

<span data-ttu-id="38773-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="38773-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38773-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38773-108">Return value</span></span>

<span data-ttu-id="38773-109">Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="38773-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="38773-110">Référence d’objet à la copie de l’objet [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="38773-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="38773-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="38773-111">Examples</span></span>

<span data-ttu-id="38773-112">L’exemple suivant illustre la **\_ NewEnum** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="38773-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="38773-113">L’utilisation appropriée est indiquée pour VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="38773-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="38773-114">Cette méthode ne peut pas être utilisée avec JScript.</span><span class="sxs-lookup"><span data-stu-id="38773-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="38773-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="38773-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="38773-116">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="38773-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="38773-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="38773-117">Requirements</span></span>



| <span data-ttu-id="38773-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38773-118">Requirement</span></span> | <span data-ttu-id="38773-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="38773-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38773-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38773-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38773-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38773-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="38773-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38773-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38773-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38773-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38773-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="38773-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38773-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38773-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="38773-126">DLL</span><span class="sxs-lookup"><span data-stu-id="38773-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38773-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="38773-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
