---
description: Récupère l’objet FolderItem pour un élément spécifié dans la collection.
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: FolderItems. Item, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed670ed4af3882e38faf2699429c3d1c076f3056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971891"
---
# <a name="folderitemsitem-method"></a><span data-ttu-id="2c564-103">FolderItems. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="2c564-103">FolderItems.Item method</span></span>

<span data-ttu-id="2c564-104">Récupère l’objet [**FolderItem**](folderitem.md) pour un élément spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2c564-104">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c564-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c564-105">Syntax</span></span>


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="2c564-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c564-107">*iIndex* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2c564-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c564-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="2c564-108">Type: **Variant**</span></span>

<span data-ttu-id="2c564-109">Index de base zéro de l'élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2c564-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="2c564-110">Cette valeur doit être inférieure à la valeur de la propriété [**Count**](folderitems-count.md) .</span><span class="sxs-lookup"><span data-stu-id="2c564-110">This value must be less than the value of the [**Count**](folderitems-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c564-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c564-111">Return value</span></span>

<span data-ttu-id="2c564-112">Référence d’objet à l’objet [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2c564-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="2c564-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="2c564-113">Examples</span></span>

<span data-ttu-id="2c564-114">L’exemple suivant utilise **Item** pour récupérer l’objet [**FolderItem**](folderitem.md) représentant le fichier Notepad.exe figurant dans le dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="2c564-114">The following example uses **Item** to retrieve the [**FolderItem**](folderitem.md) object representing the Notepad.exe file found in the Windows folder.</span></span> <span data-ttu-id="2c564-115">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2c564-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2c564-116">Langage</span><span class="sxs-lookup"><span data-stu-id="2c564-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



<span data-ttu-id="2c564-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="2c564-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="2c564-118">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="2c564-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsItemVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2c564-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c564-119">Requirements</span></span>



| <span data-ttu-id="2c564-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c564-120">Requirement</span></span> | <span data-ttu-id="2c564-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c564-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c564-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c564-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2c564-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c564-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2c564-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c564-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2c564-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c564-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c564-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c564-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c564-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c564-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2c564-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="2c564-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c564-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c564-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2c564-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2c564-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c564-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2c564-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c564-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c564-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c564-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="2c564-133">**FolderItems**</span></span>](folderitems.md)
</dt> </dl>

 

 




