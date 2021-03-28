---
description: Obtient ou définit la description du lien.
ms.assetid: d3a95281-fb1f-4fd4-9d26-2a6e10a36a86
title: Propriété ShellLinkObject. Description (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Description
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aff08831bf194da5c7ce958e5a0746abdd533dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973287"
---
# <a name="shelllinkobjectdescription-property"></a><span data-ttu-id="72b14-103">Propriété ShellLinkObject. Description</span><span class="sxs-lookup"><span data-stu-id="72b14-103">ShellLinkObject.Description property</span></span>

<span data-ttu-id="72b14-104">Obtient ou définit la description du lien.</span><span class="sxs-lookup"><span data-stu-id="72b14-104">Gets or sets the description of the link.</span></span>

<span data-ttu-id="72b14-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="72b14-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b14-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72b14-106">Syntax</span></span>


```JScript
strDescription = ShellLinkObject.Description
ShellLinkObject.Description(sDescription) = strDescription
```



## <a name="property-value"></a><span data-ttu-id="72b14-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="72b14-107">Property value</span></span>

<span data-ttu-id="72b14-108">Description du lien.</span><span class="sxs-lookup"><span data-stu-id="72b14-108">the link's description.</span></span>

## <a name="examples"></a><span data-ttu-id="72b14-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="72b14-109">Examples</span></span>

<span data-ttu-id="72b14-110">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="72b14-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="72b14-111">Langage</span><span class="sxs-lookup"><span data-stu-id="72b14-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectDescriptionJ()
    {
        var objShell = new ActiveXObject("shell.application");
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
                    var szDescription;
                    
                    // Get the description for the ShellLinkObject.
                    szDescription = objShellLink.Description;
                    alert(szDescription);
                    
                    // Set the description for the ShellLinkObject.
                    objShellLink.Description = "Test"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="72b14-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="72b14-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectDescriptionVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim szDescription
                                
                                'Get the description for the ShellLinkObject.
                                szDescription = objShellLink.Description
                                alert(szDescription)
                                
                                'Set the description for the ShellLinkObject.
                                objShellLink.Description = "Test"
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="72b14-113">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="72b14-113">Visual Basic:</span></span>


```VB
rivate Sub fnShellLinkObjectDescriptionVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim szDescription As String
                            
                            'Get the description for the ShellLinkObject.
                            szDescription = objShellLink.Description
                            Debug.Print szDescription
                            
                            'Set the description for the ShellLinkObject.
                            objShellLink.Description = "Test"
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="72b14-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="72b14-114">Requirements</span></span>



| <span data-ttu-id="72b14-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72b14-115">Requirement</span></span> | <span data-ttu-id="72b14-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="72b14-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b14-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b14-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72b14-118">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72b14-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="72b14-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b14-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72b14-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72b14-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="72b14-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="72b14-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b14-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="72b14-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="72b14-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72b14-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="72b14-125">DLL</span><span class="sxs-lookup"><span data-stu-id="72b14-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b14-126"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="72b14-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




