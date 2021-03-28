---
description: Contient les arguments d’un lien.
ms.assetid: 938db958-4b59-4dd6-ac56-f21db05ec989
title: ShellLinkObject. arguments, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Arguments
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c9b8a32eb4b935b5164ef91bf299777b36d7e53d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209935"
---
# <a name="shelllinkobjectarguments-property"></a><span data-ttu-id="b2857-103">ShellLinkObject. arguments, propriété</span><span class="sxs-lookup"><span data-stu-id="b2857-103">ShellLinkObject.Arguments property</span></span>

<span data-ttu-id="b2857-104">Contient les arguments d’un lien.</span><span class="sxs-lookup"><span data-stu-id="b2857-104">Contains a link's arguments.</span></span>

<span data-ttu-id="b2857-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b2857-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2857-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2857-106">Syntax</span></span>


```JScript
strArguments = ShellLinkObject.Arguments
ShellLinkObject.Arguments(sArguments) = strArguments
```



## <a name="property-value"></a><span data-ttu-id="b2857-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b2857-107">Property value</span></span>

<span data-ttu-id="b2857-108">arguments du lien.</span><span class="sxs-lookup"><span data-stu-id="b2857-108">the link's arguments.</span></span>

## <a name="examples"></a><span data-ttu-id="b2857-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="b2857-109">Examples</span></span>

<span data-ttu-id="b2857-110">L’exemple suivant utilise des **arguments** pour récupérer les arguments d’un lien vers Internet Explorer trouvé dans le menu Démarrer de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2857-110">The following example uses **Arguments** to retrieve the arguments for a link to Internet Explorer found in the user's Start menu.</span></span> <span data-ttu-id="b2857-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b2857-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b2857-112">Langage</span><span class="sxs-lookup"><span data-stu-id="b2857-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectArgumentJ()
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
                    var szArguments;
                    
                    // Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments;
                    alert(szArguments);
                    
                    // Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="b2857-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="b2857-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectArgumentVB()
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
                    dim szArguments
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    alert(szArguments)
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
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



<span data-ttu-id="b2857-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="b2857-114">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectArgumentsVB()
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
                    Dim szArguments As String
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    Debug.Print szArguments
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                End If

                Set objShellLink = Nothing
            End If

            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b2857-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b2857-115">Requirements</span></span>



| <span data-ttu-id="b2857-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2857-116">Requirement</span></span> | <span data-ttu-id="b2857-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2857-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2857-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2857-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2857-119">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2857-119">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b2857-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2857-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2857-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2857-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b2857-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2857-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2857-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2857-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b2857-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="b2857-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2857-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2857-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b2857-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b2857-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2857-127"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b2857-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




