---
description: Déplace un élément ou des éléments vers ce dossier.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Méthode Folder. MoveHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749180"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="5c633-103">Folder. MoveHere, méthode</span><span class="sxs-lookup"><span data-stu-id="5c633-103">Folder.MoveHere method</span></span>

<span data-ttu-id="5c633-104">Déplace un élément ou des éléments vers ce dossier.</span><span class="sxs-lookup"><span data-stu-id="5c633-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c633-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c633-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="5c633-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c633-107">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c633-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c633-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="5c633-108">Type: **Variant**</span></span>

<span data-ttu-id="5c633-109">Élément ou éléments à déplacer.</span><span class="sxs-lookup"><span data-stu-id="5c633-109">The item or items to move.</span></span> <span data-ttu-id="5c633-110">Il peut s’agir d’une chaîne qui représente un nom de fichier, un objet [**FolderItem**](folderitem.md) ou un objet [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="5c633-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5c633-111">*vOptions* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5c633-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c633-112">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="5c633-112">Type: **Variant**</span></span>

<span data-ttu-id="5c633-113">Options pour l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="5c633-113">Options for the move operation.</span></span> <span data-ttu-id="5c633-114">Cette valeur peut être zéro ou une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5c633-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="5c633-115">Ces valeurs sont basées sur les indicateurs définis pour une utilisation avec le membre **fFlags** de la structure C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="5c633-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="5c633-116">Ces indicateurs ne sont pas définis comme tels pour Visual Basic, VBScript ou JScript. vous devez donc les définir vous-même ou utiliser leurs équivalents numériques.</span><span class="sxs-lookup"><span data-stu-id="5c633-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="5c633-117">(4)</span><span class="sxs-lookup"><span data-stu-id="5c633-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-118">Ne pas afficher de boîte de dialogue de progression.</span><span class="sxs-lookup"><span data-stu-id="5c633-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-119">(8)</span><span class="sxs-lookup"><span data-stu-id="5c633-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-120">Donnez au fichier utilisé un nouveau nom dans une opération de déplacement, de copie ou de changement de nom si un fichier portant le nom cible existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5c633-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-121">(16)</span><span class="sxs-lookup"><span data-stu-id="5c633-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-122">Répondre avec « Oui pour tout » pour une boîte de dialogue qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5c633-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-123">(64)</span><span class="sxs-lookup"><span data-stu-id="5c633-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-124">Conserver les informations d’annulation, si possible.</span><span class="sxs-lookup"><span data-stu-id="5c633-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-125">(128)</span><span class="sxs-lookup"><span data-stu-id="5c633-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-126">Effectue l’opération sur les fichiers uniquement si un nom de fichier générique ( \* . \* ) est spécifié.</span><span class="sxs-lookup"><span data-stu-id="5c633-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-127">(256)</span><span class="sxs-lookup"><span data-stu-id="5c633-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-128">Affiche une boîte de dialogue de progression, mais n’affiche pas les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5c633-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-129">(512)</span><span class="sxs-lookup"><span data-stu-id="5c633-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-130">Ne confirmez pas la création d’un nouveau répertoire si l’opération requiert la création d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="5c633-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-131">(1024)</span><span class="sxs-lookup"><span data-stu-id="5c633-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-132">N’affiche pas d’interface utilisateur si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="5c633-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-133">(2048)</span><span class="sxs-lookup"><span data-stu-id="5c633-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="5c633-134">Version 4,71.</span><span class="sxs-lookup"><span data-stu-id="5c633-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="5c633-135">Ne copiez pas les attributs de sécurité du fichier.</span><span class="sxs-lookup"><span data-stu-id="5c633-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-136">(4096)</span><span class="sxs-lookup"><span data-stu-id="5c633-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="5c633-137">Ne fonctionne que dans le répertoire local.</span><span class="sxs-lookup"><span data-stu-id="5c633-137">Only operate in the local directory.</span></span> <span data-ttu-id="5c633-138">Ne pas utiliser de manière récursive dans les sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="5c633-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="5c633-139">(9182)</span><span class="sxs-lookup"><span data-stu-id="5c633-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="5c633-140">Version 5,0.</span><span class="sxs-lookup"><span data-stu-id="5c633-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="5c633-141">Ne pas déplacer les fichiers connectés en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="5c633-141">Do not move connected files as a group.</span></span> <span data-ttu-id="5c633-142">Déplacer uniquement les fichiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5c633-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c633-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c633-143">Return value</span></span>

<span data-ttu-id="5c633-144">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5c633-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c633-145">Notes</span><span class="sxs-lookup"><span data-stu-id="5c633-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c633-146">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="5c633-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="5c633-147">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="5c633-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="5c633-148">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="5c633-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5c633-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="5c633-149">Examples</span></span>

<span data-ttu-id="5c633-150">L’exemple suivant utilise **MoveHere** pour déplacer le fichier Temp.txt du répertoire racine du lecteur c vers le dossier c : \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="5c633-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="5c633-151">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c633-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5c633-152">Langage</span><span class="sxs-lookup"><span data-stu-id="5c633-152">JScript:</span></span>


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



<span data-ttu-id="5c633-153">VBScript</span><span class="sxs-lookup"><span data-stu-id="5c633-153">VBScript:</span></span>


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="5c633-154">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="5c633-154">Visual Basic:</span></span>


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5c633-155">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5c633-155">Requirements</span></span>



| <span data-ttu-id="5c633-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c633-156">Requirement</span></span> | <span data-ttu-id="5c633-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c633-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c633-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c633-158">Minimum supported client</span></span><br/> | <span data-ttu-id="5c633-159">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c633-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c633-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c633-160">Minimum supported server</span></span><br/> | <span data-ttu-id="5c633-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c633-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5c633-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c633-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c633-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c633-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5c633-164">MIDL</span><span class="sxs-lookup"><span data-stu-id="5c633-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c633-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c633-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5c633-166">DLL</span><span class="sxs-lookup"><span data-stu-id="5c633-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c633-167"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5c633-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




