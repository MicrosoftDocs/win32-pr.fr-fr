---
description: Contient la cible de l’objet de lien.
ms.assetid: 26da562b-a1d6-4150-9d9a-05b11e3972d9
title: Propriété IShellLinkDual2. Target (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2.Target
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8e5f29623cf94ef5f17f06e52337928c0c345e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972326"
---
# <a name="ishelllinkdual2target-property"></a><span data-ttu-id="d624f-103">IShellLinkDual2. Target, propriété</span><span class="sxs-lookup"><span data-stu-id="d624f-103">IShellLinkDual2.Target property</span></span>

<span data-ttu-id="d624f-104">Contient la cible de l’objet de lien.</span><span class="sxs-lookup"><span data-stu-id="d624f-104">Contains the link object's target.</span></span>

<span data-ttu-id="d624f-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d624f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d624f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d624f-106">Syntax</span></span>


```JScript
Target = IShellLinkDual2.Target
```



## <a name="property-value"></a><span data-ttu-id="d624f-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d624f-107">Property value</span></span>

<span data-ttu-id="d624f-108">Expression d’objet qui prend la valeur de l’objet [**FolderItem**](folderitem.md) de la cible.</span><span class="sxs-lookup"><span data-stu-id="d624f-108">An object expression that evaluates to the target's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="d624f-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="d624f-109">Examples</span></span>

<span data-ttu-id="d624f-110">L’exemple suivant utilise la **cible** pour récupérer la cible d’un raccourci vers Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d624f-110">The following example uses **Target** to retrieve the target of a shortcut to Internet Explorer.</span></span> <span data-ttu-id="d624f-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d624f-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d624f-112">Langage</span><span class="sxs-lookup"><span data-stu-id="d624f-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellLinkDual2TargetJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
                
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                        
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var objTargetItem;
                            
                    objTargetItem = objShellLink.Target;
                    if (objTargetItem != null)
                    {
                        // Add code here.
                    }
                }
            }
        }
    }
</script>
```



<span data-ttu-id="d624f-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="d624f-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellLinkDual2TargetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objShellLink
                    
                    set objShellLink = objFolderItem.GetLink
                        if (not objShellLink is nothing) then
                            dim objTargetItem
                            
                            set objTargetItem = objShellLink.Target
                                if (not objTargetItem is nothing) then
                                    'Add code here.
                                end if
                            set objTargetItem = nothing
                        end if
                    set objShellLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d624f-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="d624f-114">Visual Basic:</span></span>


```VB
Private Sub fnIShellLinkDual2TargetVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfPROGRAMS
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
                
        Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
        If (Not objFolderItem Is Nothing) Then
            Dim objShellLink As ShellLinkObject
            
            Set objShellLink = objFolderItem.GetLink
                If (Not objShellLink Is Nothing) Then
                    Dim objTargetItem As FolderItem
                    
                    Set objTargetItem = objShellLink.Target
                        If (Not objTargetItem Is Nothing) Then
                            'Add code here
                        End If
                    Set objTargetItem = Nothing
                End If
            Set objShellLink = Nothing
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d624f-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d624f-115">Requirements</span></span>



| <span data-ttu-id="d624f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d624f-116">Requirement</span></span> | <span data-ttu-id="d624f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d624f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d624f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d624f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d624f-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d624f-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d624f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d624f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d624f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d624f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d624f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d624f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d624f-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d624f-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d624f-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="d624f-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d624f-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d624f-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d624f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d624f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d624f-127"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d624f-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d624f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d624f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d624f-129">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="d624f-129">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)
</dt> <dt>

[<span data-ttu-id="d624f-130">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="d624f-130">**ShellLinkObject**</span></span>](shelllinkobject-object.md)
</dt> </dl>

 

 




