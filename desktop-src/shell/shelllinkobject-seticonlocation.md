---
description: Définit l’emplacement de l’icône assignée au lien.
ms.assetid: 257bb8e2-29fa-4d2f-ac2d-3497cf12959c
title: Méthode ShellLinkObject. SetIconLocation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.SetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 996f9648e9b9f59e1e84871abac1d6b37e2592d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991677"
---
# <a name="shelllinkobjectseticonlocation-method"></a><span data-ttu-id="06cdb-103">Méthode ShellLinkObject. SetIconLocation</span><span class="sxs-lookup"><span data-stu-id="06cdb-103">ShellLinkObject.SetIconLocation method</span></span>

<span data-ttu-id="06cdb-104">Définit l’emplacement de l’icône assignée au lien.</span><span class="sxs-lookup"><span data-stu-id="06cdb-104">Sets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cdb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06cdb-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.SetIconLocation(
  sPath,
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="06cdb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06cdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cdb-107">*spath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06cdb-107">*sPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cdb-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="06cdb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="06cdb-109">Chemin d’accès qualifié complet du fichier qui contient l’icône.</span><span class="sxs-lookup"><span data-stu-id="06cdb-109">The fully qualified path of the file that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="06cdb-110">*iIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06cdb-110">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cdb-111">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="06cdb-111">Type: **Integer**</span></span>

<span data-ttu-id="06cdb-112">Index de l’icône dans le fichier spécifié par *spath*.</span><span class="sxs-lookup"><span data-stu-id="06cdb-112">The index of the icon in the file specified by *sPath*.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="06cdb-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="06cdb-113">Examples</span></span>

<span data-ttu-id="06cdb-114">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="06cdb-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="06cdb-115">Langage</span><span class="sxs-lookup"><span data-stu-id="06cdb-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSetIconLocationJ()
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
                    objShellLink.SetIconLocation(objShellLink.Path, 1);
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="06cdb-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="06cdb-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSetIconLocationVB()
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
                                objShellLink.SetIconLocation objShellLink.Path, 1
                                objShellLink.Save
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



<span data-ttu-id="06cdb-117">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="06cdb-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSetIconLocationVB()
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
                            objShellLink.SetIconLocation objShellLink.Path, 1
                            objShellLink.Save
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="06cdb-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="06cdb-118">Requirements</span></span>



| <span data-ttu-id="06cdb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06cdb-119">Requirement</span></span> | <span data-ttu-id="06cdb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="06cdb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cdb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06cdb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06cdb-122">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06cdb-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06cdb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06cdb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06cdb-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06cdb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="06cdb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="06cdb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="06cdb-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06cdb-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="06cdb-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="06cdb-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06cdb-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06cdb-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="06cdb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="06cdb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06cdb-130"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="06cdb-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
