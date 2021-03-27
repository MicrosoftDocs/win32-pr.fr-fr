---
description: Contient le nom du verbe.
ms.assetid: d18fddac-eb51-4031-a572-1bfef2f757a9
title: Propriété FolderItemVerb.Name (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d352f02486f1d7304d4c474aa836401bfef635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971871"
---
# <a name="folderitemverbname-property"></a><span data-ttu-id="6bf71-103">Propriété FolderItemVerb.Name</span><span class="sxs-lookup"><span data-stu-id="6bf71-103">FolderItemVerb.Name property</span></span>

<span data-ttu-id="6bf71-104">Contient le nom du verbe.</span><span class="sxs-lookup"><span data-stu-id="6bf71-104">Contains the verb's name.</span></span>

<span data-ttu-id="6bf71-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6bf71-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf71-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bf71-106">Syntax</span></span>


```JScript
strName = FolderItemVerb.Name
```



## <a name="property-value"></a><span data-ttu-id="6bf71-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6bf71-107">Property value</span></span>

<span data-ttu-id="6bf71-108">Variable de type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) qui reçoit la propriété Name.</span><span class="sxs-lookup"><span data-stu-id="6bf71-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the Name property.</span></span>

## <a name="examples"></a><span data-ttu-id="6bf71-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="6bf71-109">Examples</span></span>

<span data-ttu-id="6bf71-110">L’exemple suivant utilise **Name** pour récupérer le nom du premier élément de la collection de verbes à laquelle le dossier de programme de l’utilisateur répond.</span><span class="sxs-lookup"><span data-stu-id="6bf71-110">The following example uses **Name** to retrieve the name of the first item in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="6bf71-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6bf71-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6bf71-112">Langage</span><span class="sxs-lookup"><span data-stu-id="6bf71-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbNameJ()
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
                var szReturn = "";
                
                szReturn = objVerbs.Item(0).Name;
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="6bf71-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="6bf71-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbNameVB()
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
                        dim szReturn
                        
                        szReturn = objVerbs.Item(0).Name
                        alert(szReturn)
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6bf71-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="6bf71-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbNameVB()
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
                Dim szReturn As String
                
                szReturn = objVerbs.Item(0).Name
                Debug.Print szReturn
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6bf71-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6bf71-115">Requirements</span></span>



| <span data-ttu-id="6bf71-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bf71-116">Requirement</span></span> | <span data-ttu-id="6bf71-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bf71-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf71-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bf71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf71-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bf71-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6bf71-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bf71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf71-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bf71-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6bf71-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bf71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bf71-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bf71-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6bf71-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="6bf71-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6bf71-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6bf71-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6bf71-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6bf71-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bf71-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6bf71-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
