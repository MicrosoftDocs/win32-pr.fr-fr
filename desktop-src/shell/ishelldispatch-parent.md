---
description: Récupère un objet qui représente le parent de l’objet actuel.
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: Propriété IShellDispatch. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113978"
---
# <a name="ishelldispatchparent-property"></a><span data-ttu-id="35bb9-103">IShellDispatch. Parent, propriété</span><span class="sxs-lookup"><span data-stu-id="35bb9-103">IShellDispatch.Parent property</span></span>

<span data-ttu-id="35bb9-104">Récupère un objet qui représente le parent de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="35bb9-104">Retrieves an object that represents the parent of the current object.</span></span>

<span data-ttu-id="35bb9-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="35bb9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35bb9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35bb9-106">Syntax</span></span>


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="35bb9-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="35bb9-107">Property value</span></span>

<span data-ttu-id="35bb9-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="35bb9-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="remarks"></a><span data-ttu-id="35bb9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="35bb9-109">Remarks</span></span>

<span data-ttu-id="35bb9-110">Cette propriété est implémentée et accessible via la propriété [**Shell. parent**](shell-parent.md) .</span><span class="sxs-lookup"><span data-stu-id="35bb9-110">This property is implemented and accessed through the [**Shell.Parent**](shell-parent.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="35bb9-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="35bb9-111">Examples</span></span>

<span data-ttu-id="35bb9-112">Les exemples suivants illustrent l’utilisation du **parent** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="35bb9-112">The following examples show the use of **Parent** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="35bb9-113">Langage</span><span class="sxs-lookup"><span data-stu-id="35bb9-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="35bb9-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="35bb9-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="35bb9-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="35bb9-115">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="35bb9-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="35bb9-116">Requirements</span></span>



| <span data-ttu-id="35bb9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35bb9-117">Requirement</span></span> | <span data-ttu-id="35bb9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="35bb9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35bb9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35bb9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35bb9-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35bb9-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="35bb9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35bb9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35bb9-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35bb9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35bb9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="35bb9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35bb9-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35bb9-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="35bb9-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="35bb9-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35bb9-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35bb9-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="35bb9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="35bb9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35bb9-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="35bb9-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
