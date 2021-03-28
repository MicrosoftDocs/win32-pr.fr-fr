---
description: Exécute un verbe sur le FolderItem associé au verbe.
ms.assetid: 92400fe9-e4d1-4bc9-b4ee-d2adaf38154f
title: Méthode FolderItemVerb. DoIt (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.DoIt
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0703b9403dfe9ff6600de68aaa710cd5a55c225a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971874"
---
# <a name="folderitemverbdoit-method"></a><span data-ttu-id="5cc9c-103">Méthode FolderItemVerb. DoIt</span><span class="sxs-lookup"><span data-stu-id="5cc9c-103">FolderItemVerb.DoIt method</span></span>

<span data-ttu-id="5cc9c-104">Exécute un verbe sur le [**FolderItem**](folderitem.md) associé au verbe.</span><span class="sxs-lookup"><span data-stu-id="5cc9c-104">Executes a verb on the [**FolderItem**](folderitem.md) associated with the verb.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cc9c-105">Syntax</span></span>


```JScript
FolderItemVerb.DoIt()
```



## <a name="parameters"></a><span data-ttu-id="5cc9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cc9c-106">Parameters</span></span>

<span data-ttu-id="5cc9c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5cc9c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cc9c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5cc9c-108">Return value</span></span>

<span data-ttu-id="5cc9c-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5cc9c-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="5cc9c-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="5cc9c-110">Examples</span></span>

<span data-ttu-id="5cc9c-111">L’exemple suivant utilise **doit** pour exécuter le premier verbe dans la collection de verbes à laquelle le dossier de programme de l’utilisateur répond.</span><span class="sxs-lookup"><span data-stu-id="5cc9c-111">The following example uses **DoIt** to execute the first verb in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="5cc9c-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5cc9c-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5cc9c-113">Langage</span><span class="sxs-lookup"><span data-stu-id="5cc9c-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbDoItJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                objVerbs.Item(0).DoIt();
            }
        }
    }
</script>
```



<span data-ttu-id="5cc9c-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="5cc9c-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbDoItVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        objVerbs.Item(0).DoIt
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="5cc9c-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="5cc9c-115">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbDoItVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                objVerbs.Item(0).DoIt
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5cc9c-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5cc9c-116">Requirements</span></span>



| <span data-ttu-id="5cc9c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cc9c-117">Requirement</span></span> | <span data-ttu-id="5cc9c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cc9c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc9c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cc9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc9c-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cc9c-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5cc9c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cc9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc9c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cc9c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5cc9c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cc9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc9c-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc9c-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5cc9c-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="5cc9c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5cc9c-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5cc9c-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5cc9c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5cc9c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cc9c-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5cc9c-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




