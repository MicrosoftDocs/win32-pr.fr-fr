---
description: FolderItems. Count, propriété-contient le nombre d’éléments dans la collection.
ms.assetid: 383382d5-7e3f-4b27-bebf-6b79dbe677b8
title: FolderItems. Count, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a2bde6d938bde675c52c93f09916a70ba0e21f9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089607"
---
# <a name="folderitemscount-property"></a><span data-ttu-id="c2090-103">FolderItems. Count (propriété)</span><span class="sxs-lookup"><span data-stu-id="c2090-103">FolderItems.Count property</span></span>

<span data-ttu-id="c2090-104">Contient le nombre d’éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="c2090-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="c2090-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c2090-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2090-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2090-106">Syntax</span></span>


```JScript
iCount = FolderItems.Count
```



## <a name="property-value"></a><span data-ttu-id="c2090-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c2090-107">Property value</span></span>

<span data-ttu-id="c2090-108">**Entier** qui contient une valeur pour la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="c2090-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="c2090-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="c2090-109">Examples</span></span>

<span data-ttu-id="c2090-110">L’exemple suivant utilise **Count** pour récupérer le nombre d’éléments dans le dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="c2090-110">The following example uses **Count** to retrieve the count of items in the Windows folder.</span></span> <span data-ttu-id="c2090-111">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c2090-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c2090-112">Langage</span><span class="sxs-lookup"><span data-stu-id="c2090-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsCountJ()
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
                var nCount;
                
                nCount = objFolderItems.Count;
                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="c2090-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="c2090-113">VBScript:</span></span>


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



<span data-ttu-id="c2090-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c2090-114">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c2090-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2090-115">Requirements</span></span>



| <span data-ttu-id="c2090-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2090-116">Requirement</span></span> | <span data-ttu-id="c2090-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2090-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2090-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2090-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2090-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2090-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c2090-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2090-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2090-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2090-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2090-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2090-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2090-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2090-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c2090-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="c2090-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2090-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2090-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c2090-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c2090-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2090-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c2090-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




