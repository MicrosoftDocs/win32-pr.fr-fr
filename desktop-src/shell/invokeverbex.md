---
description: Exécute un verbe sur un élément de Shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Méthode ShellFolderItem. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972451"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="44929-103">Méthode ShellFolderItem. InvokeVerbEx</span><span class="sxs-lookup"><span data-stu-id="44929-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="44929-104">Exécute un verbe sur un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="44929-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="44929-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44929-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="44929-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44929-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44929-107">*vVerb* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="44929-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44929-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="44929-108">Type: **Variant**</span></span>

<span data-ttu-id="44929-109">**Variant** qui contient la chaîne de verbes qui correspond à la commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="44929-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="44929-110">Il doit s’agir de l’une des valeurs retournées par la propriété [**Name**](folderitemverb-name.md) de l’élément.</span><span class="sxs-lookup"><span data-stu-id="44929-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="44929-111">Si aucun verbe n’est spécifié, le verbe par défaut est exécuté.</span><span class="sxs-lookup"><span data-stu-id="44929-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="44929-112">*vArgs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="44929-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44929-113">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="44929-113">Type: **Variant**</span></span>

<span data-ttu-id="44929-114">**Variant** qui se compose d’une chaîne avec un ou plusieurs arguments de la commande spécifiée par *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="44929-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="44929-115">Le format de cette chaîne dépend du verbe particulier.</span><span class="sxs-lookup"><span data-stu-id="44929-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44929-116">Notes</span><span class="sxs-lookup"><span data-stu-id="44929-116">Remarks</span></span>

<span data-ttu-id="44929-117">Un verbe est une chaîne utilisée pour spécifier une action particulière prise en charge par un élément.</span><span class="sxs-lookup"><span data-stu-id="44929-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="44929-118">En règle générale, l’appel d’un verbe lance une application associée.</span><span class="sxs-lookup"><span data-stu-id="44929-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="44929-119">Par exemple, l’appel du verbe **Open** sur un fichier. txt ouvre normalement le fichier avec un éditeur de texte, généralement Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="44929-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="44929-120">L’objet [**FolderItemVerbs**](folderitemverbs.md) représente la collection de verbes associée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="44929-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="44929-121">Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md).</span><span class="sxs-lookup"><span data-stu-id="44929-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="44929-122">Cette méthode est similaire à [**InvokeVerb**](folderitem-invokeverb.md), mais elle vous permet de spécifier des arguments pour la commande, ainsi que pour la commande elle-même.</span><span class="sxs-lookup"><span data-stu-id="44929-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="44929-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="44929-123">Examples</span></span>

<span data-ttu-id="44929-124">Les exemples suivants illustrent l’utilisation appropriée de cette méthode dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="44929-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="44929-125">Langage</span><span class="sxs-lookup"><span data-stu-id="44929-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="44929-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="44929-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
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
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="44929-127">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="44929-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="44929-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44929-128">Requirements</span></span>



| <span data-ttu-id="44929-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44929-129">Requirement</span></span> | <span data-ttu-id="44929-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="44929-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44929-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44929-131">Minimum supported client</span></span><br/> | <span data-ttu-id="44929-132">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44929-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44929-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44929-133">Minimum supported server</span></span><br/> | <span data-ttu-id="44929-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44929-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="44929-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="44929-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="44929-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="44929-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="44929-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="44929-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44929-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44929-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="44929-139">DLL</span><span class="sxs-lookup"><span data-stu-id="44929-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44929-140"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="44929-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44929-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44929-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44929-142">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="44929-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="44929-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="44929-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




