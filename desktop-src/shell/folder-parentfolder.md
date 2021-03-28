---
description: Contient l’objet dossier parent.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Folder. ParentFolder, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951946"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="44db8-103">Propriété Folder. ParentFolder</span><span class="sxs-lookup"><span data-stu-id="44db8-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="44db8-104">Contient l’objet [**dossier**](folder.md) parent.</span><span class="sxs-lookup"><span data-stu-id="44db8-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="44db8-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="44db8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44db8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44db8-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="44db8-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="44db8-107">Property value</span></span>

<span data-ttu-id="44db8-108">Référence d’objet à l’objet ParentFolder.</span><span class="sxs-lookup"><span data-stu-id="44db8-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44db8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="44db8-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44db8-110">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="44db8-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="44db8-111">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="44db8-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="44db8-112">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="44db8-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="44db8-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="44db8-113">Examples</span></span>

<span data-ttu-id="44db8-114">L’exemple suivant illustre l’utilisation correcte de **ParentFolder** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="44db8-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="44db8-115">Langage</span><span class="sxs-lookup"><span data-stu-id="44db8-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



<span data-ttu-id="44db8-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="44db8-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="44db8-117">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="44db8-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="44db8-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44db8-118">Requirements</span></span>



| <span data-ttu-id="44db8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44db8-119">Requirement</span></span> | <span data-ttu-id="44db8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="44db8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44db8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44db8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44db8-122">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44db8-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44db8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44db8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44db8-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44db8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44db8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="44db8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44db8-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="44db8-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="44db8-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="44db8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44db8-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44db8-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="44db8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="44db8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44db8-130"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="44db8-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




