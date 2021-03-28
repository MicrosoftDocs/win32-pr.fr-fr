---
description: Obtient ou définit le répertoire de travail spécifié dans le lien.
ms.assetid: c3820deb-9f00-42a9-ab0e-c0f6389e9f29
title: ShellLinkObject. WorkingDirectory, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.WorkingDirectory
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d8788899a06179056cd871b68e4e64566bcd5ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319426"
---
# <a name="shelllinkobjectworkingdirectory-property"></a><span data-ttu-id="caeb4-103">ShellLinkObject. WorkingDirectory, propriété</span><span class="sxs-lookup"><span data-stu-id="caeb4-103">ShellLinkObject.WorkingDirectory property</span></span>

<span data-ttu-id="caeb4-104">Obtient ou définit le répertoire de travail spécifié dans le lien.</span><span class="sxs-lookup"><span data-stu-id="caeb4-104">Gets or sets the working directory specified in the link.</span></span>

<span data-ttu-id="caeb4-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="caeb4-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="caeb4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caeb4-106">Syntax</span></span>


```JScript
strWorkingDirectory = ShellLinkObject.WorkingDirectory
ShellLinkObject.WorkingDirectory(sWorkingDirectory) = strWorkingDirectory
```



## <a name="property-value"></a><span data-ttu-id="caeb4-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="caeb4-107">Property value</span></span>

<span data-ttu-id="caeb4-108">chemin d’accès complet du répertoire de travail du lien.</span><span class="sxs-lookup"><span data-stu-id="caeb4-108">the fully qualified path of the link's working directory.</span></span>

## <a name="examples"></a><span data-ttu-id="caeb4-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="caeb4-109">Examples</span></span>

<span data-ttu-id="caeb4-110">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="caeb4-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="caeb4-111">Langage</span><span class="sxs-lookup"><span data-stu-id="caeb4-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectWorkingDirectoryJ()
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
                    var szDirectory;
                    
                    // Get the working directory for the ShellLinkObject.
                    szDirectory = objShellLink.WorkingDirectory;
                    alert(szDirectory);
                    
                    // Set the working directory for the ShellLinkObject.
                    objShellLink.WorkingDirectory = "";
                }
            }
        }
    }
</script>
```



<span data-ttu-id="caeb4-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="caeb4-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectWorkingDirectoryVB()
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
                                dim szDirectory
                                
                                'Get the working directory.
                                szDirectory = objShellLink.WorkingDirectory
                                alert(szDirectory)
                                
                                'Set the working directory.
                                objShellLink.WorkingDirectory = ""
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



<span data-ttu-id="caeb4-113">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="caeb4-113">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectWorkingDirectoryVB()
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
                            Dim szDirectory As String
                            
                            'Get the working directory.
                            szDirectory = objShellLink.WorkingDirectory
                            Debug.Print szDirectory
                            
                            'Set the working directory.
                            objShellLink.WorkingDirectory = ""
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="caeb4-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="caeb4-114">Requirements</span></span>



| <span data-ttu-id="caeb4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caeb4-115">Requirement</span></span> | <span data-ttu-id="caeb4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="caeb4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caeb4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caeb4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="caeb4-118">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caeb4-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="caeb4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caeb4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="caeb4-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caeb4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="caeb4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="caeb4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="caeb4-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="caeb4-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="caeb4-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="caeb4-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caeb4-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="caeb4-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="caeb4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="caeb4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caeb4-126"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="caeb4-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




