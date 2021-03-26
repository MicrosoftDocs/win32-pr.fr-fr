---
description: Copie un ou des éléments dans un dossier.
title: Méthode Folder. CopyHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991592"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="cbcbb-103">Folder. CopyHere, méthode</span><span class="sxs-lookup"><span data-stu-id="cbcbb-103">Folder.CopyHere method</span></span>

<span data-ttu-id="cbcbb-104">Copie un ou des éléments dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbcbb-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="cbcbb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbcbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbcbb-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="cbcbb-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="cbcbb-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="cbcbb-108">Type: **Variant**</span></span>

<span data-ttu-id="cbcbb-109">Élément ou éléments à copier.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-109">The item or items to copy.</span></span> <span data-ttu-id="cbcbb-110">Il peut s’agir d’une chaîne qui représente un nom de fichier, un objet [**FolderItem**](folderitem.md) ou un objet [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="cbcbb-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbcbb-111">*vOptions* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cbcbb-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcbb-112">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="cbcbb-112">Type: **Variant**</span></span>

<span data-ttu-id="cbcbb-113">Options pour l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-113">Options for the copy operation.</span></span> <span data-ttu-id="cbcbb-114">Cette valeur peut être zéro ou une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="cbcbb-115">Ces valeurs sont basées sur les indicateurs définis pour une utilisation avec le membre **fFlags** de la structure C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="cbcbb-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="cbcbb-116">Chaque espace de noms de Shell doit fournir sa propre implémentation de ces indicateurs, et chaque espace de noms peut choisir d’ignorer certains ou même tous ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="cbcbb-117">Ces indicateurs ne sont pas définis par nom pour Visual Basic, VBScript ou JScript. vous devez donc les définir vous-même ou utiliser leurs équivalents numériques.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="cbcbb-118">Dans certains cas, tels que les fichiers compressés (. zip), certains indicateurs d’option peuvent être ignorés par la conception.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="cbcbb-119">(4)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-120">Ne pas afficher de boîte de dialogue de progression.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-121">(8)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-122">Donnez au fichier utilisé un nouveau nom dans une opération de déplacement, de copie ou de changement de nom si un fichier portant le nom cible existe déjà.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-123">(16)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-124">Répondre avec « Oui pour tout » pour une boîte de dialogue qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-125">(64)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-126">Conserver les informations d’annulation, si possible.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-127">(128)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-128">Effectue l’opération sur les fichiers uniquement si un nom de fichier générique ( \* . \* ) est spécifié.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-129">(256)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-130">Affiche une boîte de dialogue de progression, mais n’affiche pas les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-131">(512)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-132">Ne confirmez pas la création d’un nouveau répertoire si l’opération requiert la création d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-134">N’affiche pas d’interface utilisateur si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="cbcbb-136">Version 4,71.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="cbcbb-137">Ne copiez pas les attributs de sécurité du fichier.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="cbcbb-139">Ne fonctionne que dans le répertoire local.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-139">Only operate in the local directory.</span></span> <span data-ttu-id="cbcbb-140">Ne pas utiliser de manière récursive dans les sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="cbcbb-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="cbcbb-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="cbcbb-142">Version 5,0.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="cbcbb-143">Ne copiez pas les fichiers connectés en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="cbcbb-144">Copiez uniquement les fichiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbcbb-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbcbb-145">Return value</span></span>

<span data-ttu-id="cbcbb-146">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbcbb-147">Notes</span><span class="sxs-lookup"><span data-stu-id="cbcbb-147">Remarks</span></span>

<span data-ttu-id="cbcbb-148">Aucune notification n’est donnée au programme appelant pour indiquer que la copie est terminée.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="cbcbb-149">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="cbcbb-150">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="cbcbb-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="cbcbb-151">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cbcbb-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="cbcbb-152">Examples</span></span>

<span data-ttu-id="cbcbb-153">L’exemple suivant utilise **CopyHere** pour copier le fichier Autoexec.bat du répertoire racine vers le répertoire C : \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="cbcbb-154">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cbcbb-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cbcbb-155">Langage</span><span class="sxs-lookup"><span data-stu-id="cbcbb-155">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



<span data-ttu-id="cbcbb-156">VBScript</span><span class="sxs-lookup"><span data-stu-id="cbcbb-156">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



<span data-ttu-id="cbcbb-157">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="cbcbb-157">Visual Basic:</span></span>


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cbcbb-158">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cbcbb-158">Requirements</span></span>



| <span data-ttu-id="cbcbb-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbcbb-159">Requirement</span></span> | <span data-ttu-id="cbcbb-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbcbb-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcbb-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbcbb-161">Minimum supported client</span></span><br/> | <span data-ttu-id="cbcbb-162">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbcbb-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cbcbb-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbcbb-163">Minimum supported server</span></span><br/> | <span data-ttu-id="cbcbb-164">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbcbb-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbcbb-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbcbb-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbcbb-166"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbcbb-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cbcbb-167">MIDL</span><span class="sxs-lookup"><span data-stu-id="cbcbb-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbcbb-168"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbcbb-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cbcbb-169">DLL</span><span class="sxs-lookup"><span data-stu-id="cbcbb-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbcbb-170"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="cbcbb-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbcbb-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbcbb-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcbb-172">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="cbcbb-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




