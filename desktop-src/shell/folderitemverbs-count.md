---
description: Contient le nombre d’éléments de la collection.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: FolderItemVerbs. Count, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b41e78261dfc9bc72e9262615bc395a9d559e33a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991584"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="6cfd7-103">FolderItemVerbs. Count (propriété)</span><span class="sxs-lookup"><span data-stu-id="6cfd7-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="6cfd7-104">Contient le nombre d’éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="6cfd7-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="6cfd7-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6cfd7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfd7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cfd7-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="6cfd7-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6cfd7-107">Property value</span></span>

<span data-ttu-id="6cfd7-108">**Entier** qui reçoit la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="6cfd7-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="6cfd7-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="6cfd7-109">Examples</span></span>

<span data-ttu-id="6cfd7-110">L’exemple suivant utilise **Count** pour récupérer le nombre de verbes disponibles pour le dossier du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="6cfd7-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="6cfd7-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6cfd7-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6cfd7-112">Langage</span><span class="sxs-lookup"><span data-stu-id="6cfd7-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="6cfd7-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="6cfd7-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
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
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6cfd7-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="6cfd7-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
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
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6cfd7-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6cfd7-115">Requirements</span></span>



| <span data-ttu-id="6cfd7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cfd7-116">Requirement</span></span> | <span data-ttu-id="6cfd7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cfd7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfd7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cfd7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6cfd7-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cfd7-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6cfd7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cfd7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6cfd7-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cfd7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6cfd7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cfd7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cfd7-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd7-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6cfd7-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="6cfd7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cfd7-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd7-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6cfd7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6cfd7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cfd7-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd7-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




