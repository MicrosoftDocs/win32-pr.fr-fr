---
description: Récupère un objet FolderItems qui représente la collection d’éléments dans le dossier.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Méthode Folder. Items (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319138"
---
# <a name="folderitems-method"></a><span data-ttu-id="c6593-103">Méthode Folder. Items</span><span class="sxs-lookup"><span data-stu-id="c6593-103">Folder.Items method</span></span>

<span data-ttu-id="c6593-104">Récupère un objet [**FolderItems**](folderitems.md) qui représente la collection d’éléments dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="c6593-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6593-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6593-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="c6593-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6593-106">Parameters</span></span>

<span data-ttu-id="c6593-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c6593-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6593-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6593-108">Return value</span></span>

<span data-ttu-id="c6593-109">Type : **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6593-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="c6593-110">Référence d’objet à l’objet [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="c6593-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6593-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6593-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6593-112">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="c6593-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="c6593-113">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="c6593-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="c6593-114">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="c6593-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c6593-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="c6593-115">Examples</span></span>

<span data-ttu-id="c6593-116">L’exemple suivant utilise des **éléments** pour déterminer le nombre d’éléments dans le dossier C : \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="c6593-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="c6593-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c6593-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c6593-118">Langage</span><span class="sxs-lookup"><span data-stu-id="c6593-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="c6593-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="c6593-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="c6593-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c6593-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c6593-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c6593-121">Requirements</span></span>



| <span data-ttu-id="c6593-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6593-122">Requirement</span></span> | <span data-ttu-id="c6593-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6593-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6593-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6593-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6593-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6593-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6593-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6593-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6593-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6593-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6593-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6593-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6593-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6593-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c6593-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="c6593-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6593-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6593-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c6593-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c6593-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6593-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c6593-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




