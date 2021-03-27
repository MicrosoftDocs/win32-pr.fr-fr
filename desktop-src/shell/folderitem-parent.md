---
description: Obtient un objet qui représente le parent de l’élément.
ms.assetid: 612e76d8-d8bc-419c-b319-75b1f324840a
title: Propriété FolderItem. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f2da3504596c3b351318b33c929dad3b5a958165
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749164"
---
# <a name="folderitemparent-property"></a><span data-ttu-id="211f9-103">FolderItem. Parent, propriété</span><span class="sxs-lookup"><span data-stu-id="211f9-103">FolderItem.Parent property</span></span>

<span data-ttu-id="211f9-104">Obtient un objet qui représente le parent de l’élément.</span><span class="sxs-lookup"><span data-stu-id="211f9-104">Gets an object that represents the parent of the item.</span></span>

<span data-ttu-id="211f9-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="211f9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="211f9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="211f9-106">Syntax</span></span>


```JScript
objParent = FolderItem.Parent
```



## <a name="property-value"></a><span data-ttu-id="211f9-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="211f9-107">Property value</span></span>

<span data-ttu-id="211f9-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="211f9-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="211f9-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="211f9-109">Examples</span></span>

<span data-ttu-id="211f9-110">L’exemple suivant illustre l’utilisation correcte du **parent** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="211f9-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="211f9-111">Langage</span><span class="sxs-lookup"><span data-stu-id="211f9-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



<span data-ttu-id="211f9-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="211f9-112">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemParentVB()
        dim objShell
        dim objFolder2
        dim ssfWINDOWS

        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem

                set objFolderItem = objFolder2.Self
                    if (not objFolderItem is nothing) then
                        dim objParent

                        set objParent = objFolderItem.Parent
                            if (not objParent is nothing) then
                                alert("Got parent object")
                            end if
                        set objParent = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder2 = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="211f9-113">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="211f9-113">Visual Basic:</span></span>


```VB
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



## <a name="requirements"></a><span data-ttu-id="211f9-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="211f9-114">Requirements</span></span>



| <span data-ttu-id="211f9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="211f9-115">Requirement</span></span> | <span data-ttu-id="211f9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="211f9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="211f9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="211f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="211f9-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="211f9-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="211f9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="211f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="211f9-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="211f9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="211f9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="211f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="211f9-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="211f9-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="211f9-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="211f9-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="211f9-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="211f9-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="211f9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="211f9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211f9-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="211f9-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
