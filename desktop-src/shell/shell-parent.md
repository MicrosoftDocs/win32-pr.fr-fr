---
description: Obtient un objet qui représente le parent de l’objet actuel.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Propriété Shell. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973258"
---
# <a name="shellparent-property"></a><span data-ttu-id="401a0-103">Shell. Parent, propriété</span><span class="sxs-lookup"><span data-stu-id="401a0-103">Shell.Parent property</span></span>

<span data-ttu-id="401a0-104">Obtient un objet qui représente le parent de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="401a0-104">Gets an object that represents the parent of the current object.</span></span>

<span data-ttu-id="401a0-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="401a0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="401a0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="401a0-106">Syntax</span></span>


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="401a0-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="401a0-107">Property value</span></span>

<span data-ttu-id="401a0-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="401a0-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="401a0-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="401a0-109">Examples</span></span>

<span data-ttu-id="401a0-110">L’exemple suivant illustre l’utilisation correcte du **parent** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="401a0-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="401a0-111">Langage</span><span class="sxs-lookup"><span data-stu-id="401a0-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="401a0-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="401a0-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="401a0-113">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="401a0-113">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="401a0-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="401a0-114">Requirements</span></span>



| <span data-ttu-id="401a0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="401a0-115">Requirement</span></span> | <span data-ttu-id="401a0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="401a0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="401a0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="401a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="401a0-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="401a0-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="401a0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="401a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="401a0-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="401a0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="401a0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="401a0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="401a0-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="401a0-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="401a0-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="401a0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="401a0-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="401a0-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="401a0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="401a0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="401a0-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="401a0-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
