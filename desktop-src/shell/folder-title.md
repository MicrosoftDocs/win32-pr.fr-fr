---
description: Contient le titre du dossier.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Propriété Folder. title (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973214"
---
# <a name="foldertitle-property"></a><span data-ttu-id="df549-103">Propriété dossier. title</span><span class="sxs-lookup"><span data-stu-id="df549-103">Folder.Title property</span></span>

<span data-ttu-id="df549-104">Contient le titre du dossier.</span><span class="sxs-lookup"><span data-stu-id="df549-104">Contains the title of the folder.</span></span>

<span data-ttu-id="df549-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="df549-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df549-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df549-106">Syntax</span></span>


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a><span data-ttu-id="df549-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="df549-107">Property value</span></span>

<span data-ttu-id="df549-108">Chaîne contenant le titre de l’objet.</span><span class="sxs-lookup"><span data-stu-id="df549-108">A string containing the object's title.</span></span>

## <a name="remarks"></a><span data-ttu-id="df549-109">Notes</span><span class="sxs-lookup"><span data-stu-id="df549-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="df549-110">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="df549-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="df549-111">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="df549-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="df549-112">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="df549-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="df549-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="df549-113">Examples</span></span>

<span data-ttu-id="df549-114">L’exemple suivant utilise **title** pour récupérer le titre du dossier contenant les groupes de programmes de l’utilisateur (généralement « programmes »).</span><span class="sxs-lookup"><span data-stu-id="df549-114">The following example uses **Title** to retrieve the title of the folder holding the user's program groups (usually "Programs").</span></span> <span data-ttu-id="df549-115">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="df549-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="df549-116">Langage</span><span class="sxs-lookup"><span data-stu-id="df549-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="df549-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="df549-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="df549-118">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="df549-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="df549-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="df549-119">Requirements</span></span>



| <span data-ttu-id="df549-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df549-120">Requirement</span></span> | <span data-ttu-id="df549-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="df549-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df549-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df549-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df549-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df549-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="df549-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df549-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df549-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df549-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df549-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="df549-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df549-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="df549-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="df549-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="df549-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df549-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df549-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="df549-130">DLL</span><span class="sxs-lookup"><span data-stu-id="df549-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df549-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="df549-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




