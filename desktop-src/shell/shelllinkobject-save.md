---
description: Enregistre toutes les modifications apportées au lien.
ms.assetid: 4c776c82-8eca-4c9b-9487-4a835affd2d8
title: ShellLinkObject. Save, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Save
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0283b839069464a1a059bd11ef52b522f7ec7072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991796"
---
# <a name="shelllinkobjectsave-method"></a><span data-ttu-id="28676-103">ShellLinkObject. Save, méthode</span><span class="sxs-lookup"><span data-stu-id="28676-103">ShellLinkObject.Save method</span></span>

<span data-ttu-id="28676-104">Enregistre toutes les modifications apportées au lien.</span><span class="sxs-lookup"><span data-stu-id="28676-104">Saves all changes to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="28676-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28676-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Save(
  [ sFile ]
)
```



## <a name="parameters"></a><span data-ttu-id="28676-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28676-107">*sFile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="28676-107">*sFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28676-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="28676-108">Type: **Variant**</span></span>

<span data-ttu-id="28676-109">Valeur de chaîne qui contient le chemin d’accès complet du fichier dans lequel les nouvelles informations de lien doivent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="28676-109">A string value that contains the fully qualified path of the file where the new link information is to be saved.</span></span> <span data-ttu-id="28676-110">Si aucun fichier n’est spécifié, le fichier actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="28676-110">If no file is specified, the current file is used.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="28676-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="28676-111">Examples</span></span>

<span data-ttu-id="28676-112">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="28676-112">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="28676-113">Langage</span><span class="sxs-lookup"><span data-stu-id="28676-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSaveJ()
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
                    // Making a change to the ShellLinkObject.
                    objShellLink.Description = "New Description";
                    
                    // Saving the changes.
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="28676-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="28676-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSaveVB()
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
                                'Making a change to the ShellLinkObject.
                                objShellLink.Description = "New Description"
                                
                                'Saving the changes.
                                objShellLink.Save()
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



<span data-ttu-id="28676-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="28676-115">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSaveVB()
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
                            'Making a change to the ShellLinkObject.
                            objShellLink.Description = "New Description"
                            'Saving the changes
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



## <a name="requirements"></a><span data-ttu-id="28676-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28676-116">Requirements</span></span>



| <span data-ttu-id="28676-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28676-117">Requirement</span></span> | <span data-ttu-id="28676-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="28676-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28676-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28676-119">Minimum supported client</span></span><br/> | <span data-ttu-id="28676-120">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28676-120">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="28676-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28676-121">Minimum supported server</span></span><br/> | <span data-ttu-id="28676-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28676-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="28676-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="28676-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="28676-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="28676-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="28676-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="28676-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28676-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28676-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="28676-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28676-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28676-128"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="28676-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




