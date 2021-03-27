---
description: Indique si l’élément est un raccourci.
ms.assetid: f3400f0b-5c7f-4d41-a162-1c35014082ac
title: FolderItem. IsLink, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bd4357485dce3f3d236f31797d8b2df7028f3d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861789"
---
# <a name="folderitemislink-property"></a><span data-ttu-id="3d887-103">FolderItem. IsLink, propriété</span><span class="sxs-lookup"><span data-stu-id="3d887-103">FolderItem.IsLink property</span></span>

<span data-ttu-id="3d887-104">Indique si l’élément est un raccourci.</span><span class="sxs-lookup"><span data-stu-id="3d887-104">Indicates whether the item is a shortcut.</span></span>

<span data-ttu-id="3d887-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d887-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d887-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d887-106">Syntax</span></span>


```JScript
bIsLink = FolderItem.IsLink
```



## <a name="property-value"></a><span data-ttu-id="3d887-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d887-107">Property value</span></span>

<span data-ttu-id="3d887-108">Valeur **booléenne** qui reçoit la **valeur true** si l’élément est un raccourci ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3d887-108">A **Boolean** that receives **true** if the item is a shortcut or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="3d887-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="3d887-109">Examples</span></span>

<span data-ttu-id="3d887-110">L’exemple suivant utilise **IsLink** pour déterminer si un objet particulier est un lien.</span><span class="sxs-lookup"><span data-stu-id="3d887-110">The following example uses **IsLink** to determine whether a particular object is a link.</span></span> <span data-ttu-id="3d887-111">Dans ce cas, l’objet est un raccourci vers Internet Explorer et doit donc retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="3d887-111">In this case, the object is a shortcut to Internet Explorer and so should return **true**.</span></span> <span data-ttu-id="3d887-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3d887-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3d887-113">Langage</span><span class="sxs-lookup"><span data-stu-id="3d887-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsLinkJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfPROGRAMS = 2;
        
        objFolder2 = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsLink;
            }
        }
    }
</script>
```



<span data-ttu-id="3d887-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="3d887-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsLinkVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfPROGRAMS
                
            ssfPROGRAMS = 2
            set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsLink
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3d887-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="3d887-115">Visual Basic:</span></span>


```VB
Private Sub fnIsLinkVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsLink
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3d887-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3d887-116">Requirements</span></span>



| <span data-ttu-id="3d887-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d887-117">Requirement</span></span> | <span data-ttu-id="3d887-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d887-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d887-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d887-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d887-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d887-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d887-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d887-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d887-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d887-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d887-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d887-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d887-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d887-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3d887-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="3d887-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d887-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d887-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3d887-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3d887-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d887-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3d887-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




