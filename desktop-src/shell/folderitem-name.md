---
description: Définit ou obtient le nom de l’élément.
ms.assetid: 079efc8d-3d08-48b1-bdb1-83f4b89fd633
title: Propriété FolderItem.Name (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5eb757455b8bbbd4161eae477ca4677eef4fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861786"
---
# <a name="folderitemname-property"></a><span data-ttu-id="46536-103">Propriété FolderItem.Name</span><span class="sxs-lookup"><span data-stu-id="46536-103">FolderItem.Name property</span></span>

<span data-ttu-id="46536-104">Définit ou obtient le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="46536-104">Sets or gets the item's name.</span></span>

<span data-ttu-id="46536-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="46536-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46536-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46536-106">Syntax</span></span>


```JScript
strName = FolderItem.Name
FolderItem.Name = strName
```



## <a name="property-value"></a><span data-ttu-id="46536-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="46536-107">Property value</span></span>

<span data-ttu-id="46536-108">Variable de type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) qui spécifie ou reçoit le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="46536-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that specifies or receives the item's name.</span></span>

## <a name="examples"></a><span data-ttu-id="46536-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="46536-109">Examples</span></span>

<span data-ttu-id="46536-110">L’exemple suivant utilise **Name** pour récupérer le nom du fichier Autoexec.bat, puis réinitialisez le nom sur Test.bat.</span><span class="sxs-lookup"><span data-stu-id="46536-110">The following example uses **Name** to retrieve the name of the Autoexec.bat file, then reset the name to Test.bat.</span></span> <span data-ttu-id="46536-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="46536-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="46536-112">Langage</span><span class="sxs-lookup"><span data-stu-id="46536-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnNameGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        
        objFolder2 = objShell.NameSpace("C:\\");
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Name;
                objFolderItem.Name = "TEST.BAT";
            }
        }
    }
</script>
```



<span data-ttu-id="46536-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="46536-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnNameGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
                
            set objFolder2 = objShell.NameSpace("C:\")
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="46536-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="46536-114">Visual Basic:</span></span>


```VB
Private Sub fnNameGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\")
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
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



## <a name="requirements"></a><span data-ttu-id="46536-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46536-115">Requirements</span></span>



| <span data-ttu-id="46536-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46536-116">Requirement</span></span> | <span data-ttu-id="46536-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="46536-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46536-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46536-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46536-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46536-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46536-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46536-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46536-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46536-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46536-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="46536-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="46536-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46536-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="46536-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="46536-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46536-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46536-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="46536-126">DLL</span><span class="sxs-lookup"><span data-stu-id="46536-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46536-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="46536-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
