---
description: Exécute un verbe sur l’élément.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Méthode FolderItem. InvokeVerb (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524479"
---
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="e469c-103">Méthode FolderItem. InvokeVerb</span><span class="sxs-lookup"><span data-stu-id="e469c-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="e469c-104">Exécute un verbe sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="e469c-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e469c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e469c-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="e469c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e469c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e469c-107">*vVerb* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e469c-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e469c-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e469c-108">Type: **Variant**</span></span>

<span data-ttu-id="e469c-109">Chaîne qui spécifie le verbe à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e469c-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="e469c-110">Il doit s’agir de l’une des valeurs retournées par la propriété [**FolderItemVerb.Name**](folderitemverb-name.md) de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e469c-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="e469c-111">Si aucun verbe n’est spécifié, le verbe par défaut est appelé.</span><span class="sxs-lookup"><span data-stu-id="e469c-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e469c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e469c-112">Return value</span></span>

<span data-ttu-id="e469c-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e469c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e469c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e469c-114">Remarks</span></span>

<span data-ttu-id="e469c-115">Un verbe est une chaîne utilisée pour spécifier une action particulière prise en charge par un élément.</span><span class="sxs-lookup"><span data-stu-id="e469c-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="e469c-116">L’appel d’un verbe équivaut à sélectionner une commande dans le menu contextuel d’un élément.</span><span class="sxs-lookup"><span data-stu-id="e469c-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="e469c-117">En règle générale, l’appel d’un verbe lance une application associée.</span><span class="sxs-lookup"><span data-stu-id="e469c-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="e469c-118">Par exemple, l’appel du verbe « Open » sur un fichier. txt ouvre le fichier avec un éditeur de texte, généralement Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="e469c-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="e469c-119">Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md) .</span><span class="sxs-lookup"><span data-stu-id="e469c-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="e469c-120">L’objet [**FolderItemVerbs**](folderitemverbs.md) représente la collection de verbes associée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="e469c-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="e469c-121">Le verbe par défaut peut varier pour différents éléments, mais il est généralement « Open ».</span><span class="sxs-lookup"><span data-stu-id="e469c-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="e469c-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="e469c-122">Examples</span></span>

<span data-ttu-id="e469c-123">L’exemple suivant utilise **InvokeVerb** pour appeler le verbe par défaut (« Open » dans ce cas) dans le dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="e469c-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="e469c-124">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e469c-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e469c-125">Langage</span><span class="sxs-lookup"><span data-stu-id="e469c-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



<span data-ttu-id="e469c-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="e469c-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="e469c-127">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="e469c-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
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



## <a name="requirements"></a><span data-ttu-id="e469c-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e469c-128">Requirements</span></span>



| <span data-ttu-id="e469c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e469c-129">Requirement</span></span> | <span data-ttu-id="e469c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e469c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e469c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e469c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e469c-132">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e469c-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e469c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e469c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e469c-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e469c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e469c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e469c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e469c-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e469c-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e469c-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="e469c-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e469c-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e469c-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e469c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e469c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e469c-140"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e469c-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e469c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e469c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e469c-142">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="e469c-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="e469c-143">**Verbes et adverbes**</span><span class="sxs-lookup"><span data-stu-id="e469c-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="e469c-144">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="e469c-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




