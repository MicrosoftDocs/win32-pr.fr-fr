---
description: Crée et retourne un objet FolderItem qui représente un élément spécifié.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Méthode Folder. ParseName (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749173"
---
# <a name="folderparsename-method"></a><span data-ttu-id="6f821-103">Folder. ParseName, méthode</span><span class="sxs-lookup"><span data-stu-id="6f821-103">Folder.ParseName method</span></span>

<span data-ttu-id="6f821-104">Crée et retourne un objet [**FolderItem**](folderitem.md) qui représente un élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="6f821-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f821-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f821-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="6f821-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f821-107">*bName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f821-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f821-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6f821-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6f821-109">Chaîne qui spécifie le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6f821-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f821-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f821-110">Return value</span></span>

<span data-ttu-id="6f821-111">Type : **[ **FolderItem**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6f821-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="6f821-112">Référence d’objet à l’objet [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6f821-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f821-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6f821-113">Remarks</span></span>

<span data-ttu-id="6f821-114">**ParseName** ne doit pas être utilisé pour les dossiers virtuels tels que mes documents.</span><span class="sxs-lookup"><span data-stu-id="6f821-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="6f821-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f821-115">Examples</span></span>

<span data-ttu-id="6f821-116">L’exemple suivant utilise **ParseName** pour créer un objet représentant l’élément de dossier Clock.avi dans le dossier C : \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="6f821-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="6f821-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6f821-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6f821-118">Langage</span><span class="sxs-lookup"><span data-stu-id="6f821-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="6f821-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="6f821-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6f821-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="6f821-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6f821-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f821-121">Requirements</span></span>



| <span data-ttu-id="6f821-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f821-122">Requirement</span></span> | <span data-ttu-id="6f821-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f821-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f821-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f821-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f821-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f821-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f821-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f821-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f821-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f821-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6f821-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f821-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f821-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f821-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6f821-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="6f821-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f821-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f821-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6f821-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6f821-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f821-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6f821-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
