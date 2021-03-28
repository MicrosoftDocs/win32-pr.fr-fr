---
description: Pour un fichier, définit ou obtient la date et l’heure de la dernière modification. Pour un dossier, récupère la date et l’heure de la dernière modification d’un dossier, mais ne peut pas le définir.
ms.assetid: bb60c800-863b-469b-b937-9816b8b338bf
title: FolderItem. ModifyDate, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.ModifyDate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9ea5fa6b611a0311840507fb2068d08801a5bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111734"
---
# <a name="folderitemmodifydate-property"></a><span data-ttu-id="2cfaf-104">FolderItem. ModifyDate, propriété</span><span class="sxs-lookup"><span data-stu-id="2cfaf-104">FolderItem.ModifyDate property</span></span>

<span data-ttu-id="2cfaf-105">Pour un fichier, définit ou obtient la date et l’heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-105">For a file, sets or gets the date and time that it was last modified.</span></span> <span data-ttu-id="2cfaf-106">Pour un dossier, récupère la date et l’heure de la dernière modification d’un dossier, mais ne peut pas le définir.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-106">For a folder, retrieves the date and time that a folder was last modified, but cannot set it.</span></span>

<span data-ttu-id="2cfaf-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cfaf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cfaf-108">Syntax</span></span>


```JScript
iModifyDate = FolderItem.ModifyDate
FolderItem.ModifyDate = iModifyDate
```



## <a name="property-value"></a><span data-ttu-id="2cfaf-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2cfaf-109">Property value</span></span>

<span data-ttu-id="2cfaf-110">**Date** qui spécifie ou reçoit la date et l’heure de la dernière modification de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-110">**Date** that specifies or receives the date and time that the item was last modified.</span></span>

## <a name="examples"></a><span data-ttu-id="2cfaf-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="2cfaf-111">Examples</span></span>

<span data-ttu-id="2cfaf-112">L’exemple suivant utilise **ModifyDate** pour récupérer la date de dernière modification du bloc-notes, puis le réinitialiser à une heure très longue.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-112">The following example uses **ModifyDate** to retrieve the last modified date of Notepad and then reset it to a very long time ago.</span></span> <span data-ttu-id="2cfaf-113">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-113">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2cfaf-114">Langage</span><span class="sxs-lookup"><span data-stu-id="2cfaf-114">JScript:</span></span>


```JScript
<script language="JScript">
    function fnModifyDateGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.ModifyDate;
                objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM";
            }
        }
    }
</script>
```



<span data-ttu-id="2cfaf-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="2cfaf-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnModifyDateGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2cfaf-116">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="2cfaf-116">Visual Basic:</span></span>


```VB
Private Sub fnModifyDateGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
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



## <a name="requirements"></a><span data-ttu-id="2cfaf-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2cfaf-117">Requirements</span></span>



| <span data-ttu-id="2cfaf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cfaf-118">Requirement</span></span> | <span data-ttu-id="2cfaf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cfaf-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfaf-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cfaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2cfaf-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cfaf-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2cfaf-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cfaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2cfaf-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cfaf-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cfaf-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2cfaf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cfaf-125"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cfaf-125"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2cfaf-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="2cfaf-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2cfaf-127"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2cfaf-127"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2cfaf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2cfaf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cfaf-129"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2cfaf-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




