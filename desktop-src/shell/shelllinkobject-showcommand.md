---
description: Obtient ou définit l’état d’affichage initial (dimensionné, réduit ou agrandi) de la commande du lien.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: ShellLinkObject. ShowCommand, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991805"
---
# <a name="shelllinkobjectshowcommand-property"></a><span data-ttu-id="fb941-103">ShellLinkObject. ShowCommand, propriété</span><span class="sxs-lookup"><span data-stu-id="fb941-103">ShellLinkObject.ShowCommand property</span></span>

<span data-ttu-id="fb941-104">Obtient ou définit l’état d’affichage initial (dimensionné, réduit ou agrandi) de la commande du lien.</span><span class="sxs-lookup"><span data-stu-id="fb941-104">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span>

<span data-ttu-id="fb941-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fb941-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb941-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb941-106">Syntax</span></span>


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a><span data-ttu-id="fb941-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fb941-107">Property value</span></span>

<span data-ttu-id="fb941-108">État d’affichage du lien.</span><span class="sxs-lookup"><span data-stu-id="fb941-108">the link's display state.</span></span> <span data-ttu-id="fb941-109">Il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb941-109">This can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="fb941-110">(1)</span><span class="sxs-lookup"><span data-stu-id="fb941-110">(1)</span></span>


</dt> <dd>

<span data-ttu-id="fb941-111">Active et affiche une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fb941-111">Activates and displays a window.</span></span> <span data-ttu-id="fb941-112">Si la fenêtre est réduite ou agrandie, le système la restaure à sa taille et à sa position d’origine.</span><span class="sxs-lookup"><span data-stu-id="fb941-112">If the window is minimized or maximized, the system restores it to its original size and position.</span></span>

</dd> <dt>



 <span data-ttu-id="fb941-113">(2)</span><span class="sxs-lookup"><span data-stu-id="fb941-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="fb941-114">Active la fenêtre et l’affiche sous forme de fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="fb941-114">Activates the window and displays it as a minimized window.</span></span>

</dd> <dt>



 <span data-ttu-id="fb941-115">(3)</span><span class="sxs-lookup"><span data-stu-id="fb941-115">(3)</span></span>


</dt> <dd>

<span data-ttu-id="fb941-116">Active la fenêtre et l’affiche sous la forme d’une fenêtre agrandie.</span><span class="sxs-lookup"><span data-stu-id="fb941-116">Activates the window and displays it as a maximized window.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fb941-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="fb941-117">Examples</span></span>

<span data-ttu-id="fb941-118">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fb941-118">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fb941-119">Langage</span><span class="sxs-lookup"><span data-stu-id="fb941-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
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
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



<span data-ttu-id="fb941-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="fb941-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
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
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
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



<span data-ttu-id="fb941-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="fb941-121">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectShowCommandVB()
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
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fb941-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fb941-122">Requirements</span></span>



| <span data-ttu-id="fb941-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb941-123">Requirement</span></span> | <span data-ttu-id="fb941-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb941-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb941-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb941-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb941-126">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb941-126">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fb941-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb941-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb941-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb941-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb941-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb941-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb941-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb941-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fb941-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="fb941-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb941-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb941-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fb941-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fb941-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb941-134"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fb941-134"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




