---
description: Exécute un verbe sur une collection d’objets FolderItem. Cette méthode est une extension de la méthode InvokeVerb, qui permet un contrôle supplémentaire de l’opération via un ensemble d’indicateurs.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Méthode FolderItems2. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971879"
---
# <a name="folderitems2invokeverbex-method"></a><span data-ttu-id="c3177-104">Méthode FolderItems2. InvokeVerbEx</span><span class="sxs-lookup"><span data-stu-id="c3177-104">FolderItems2.InvokeVerbEx method</span></span>

<span data-ttu-id="c3177-105">Exécute un verbe sur une collection d’objets [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c3177-105">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="c3177-106">Cette méthode est une extension de la méthode [**InvokeVerb**](folderitem-invokeverb.md) , qui permet un contrôle supplémentaire de l’opération via un ensemble d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c3177-106">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3177-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3177-107">Syntax</span></span>


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="c3177-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3177-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3177-109">*vVerb* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c3177-109">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3177-110">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="c3177-110">Type: **Variant**</span></span>

<span data-ttu-id="c3177-111">**Variant** avec la chaîne de verbe qui correspond à la commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c3177-111">A **Variant** with the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="c3177-112">Si aucun verbe n’est spécifié, le verbe par défaut est exécuté.</span><span class="sxs-lookup"><span data-stu-id="c3177-112">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="c3177-113">*vArgs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c3177-113">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3177-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="c3177-114">Type: **Variant**</span></span>

<span data-ttu-id="c3177-115">**Variant** qui se compose d’une chaîne avec un ou plusieurs arguments de la commande spécifiée par *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="c3177-115">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="c3177-116">Le format de cette chaîne dépend du verbe particulier.</span><span class="sxs-lookup"><span data-stu-id="c3177-116">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3177-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c3177-117">Remarks</span></span>

<span data-ttu-id="c3177-118">Un verbe est une chaîne utilisée pour spécifier une action particulière associée à un élément ou à une collection d’éléments.</span><span class="sxs-lookup"><span data-stu-id="c3177-118">A verb is a string used to specify a particular action associated with an item or collection of items.</span></span> <span data-ttu-id="c3177-119">En règle générale, l’appel d’un verbe lance une application associée.</span><span class="sxs-lookup"><span data-stu-id="c3177-119">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="c3177-120">Par exemple, l’appel du verbe **Open** sur un fichier. txt ouvre normalement le fichier avec un éditeur de texte, généralement Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="c3177-120">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="c3177-121">Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md).</span><span class="sxs-lookup"><span data-stu-id="c3177-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c3177-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="c3177-122">Examples</span></span>

<span data-ttu-id="c3177-123">L’exemple suivant utilise **InvokeVerbEx** pour appeler le verbe par défaut (« Open ») sur **poste de travail**.</span><span class="sxs-lookup"><span data-stu-id="c3177-123">The following example uses **InvokeVerbEx** to invoke the default verb ("open") on **My Computer**.</span></span> <span data-ttu-id="c3177-124">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c3177-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c3177-125">Langage</span><span class="sxs-lookup"><span data-stu-id="c3177-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



<span data-ttu-id="c3177-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="c3177-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="c3177-127">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c3177-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c3177-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3177-128">Requirements</span></span>



| <span data-ttu-id="c3177-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3177-129">Requirement</span></span> | <span data-ttu-id="c3177-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3177-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3177-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3177-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c3177-132">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3177-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3177-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3177-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c3177-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3177-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c3177-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3177-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3177-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3177-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c3177-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="c3177-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3177-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3177-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c3177-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c3177-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3177-140"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c3177-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3177-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3177-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3177-142">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="c3177-142">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="c3177-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="c3177-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




