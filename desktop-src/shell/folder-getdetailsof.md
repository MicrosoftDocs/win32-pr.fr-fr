---
description: Récupère des détails sur un élément dans un dossier. Par exemple, sa taille, son type ou l’heure de sa dernière modification.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Méthode Folder. GetDetailsOf (shlobj \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950891"
---
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="19dcb-104">Folder. GetDetailsOf, méthode</span><span class="sxs-lookup"><span data-stu-id="19dcb-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="19dcb-105">Récupère des détails sur un élément dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="19dcb-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="19dcb-106">Par exemple, sa taille, son type ou l’heure de sa dernière modification.</span><span class="sxs-lookup"><span data-stu-id="19dcb-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="19dcb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19dcb-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="19dcb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19dcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19dcb-109">*vItem*</span><span class="sxs-lookup"><span data-stu-id="19dcb-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="19dcb-110">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="19dcb-110">Type: **Variant**</span></span>

<span data-ttu-id="19dcb-111">Élément pour lequel les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="19dcb-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="19dcb-112">Il doit s’agir d’un objet [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="19dcb-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="19dcb-113">*iColumn*</span><span class="sxs-lookup"><span data-stu-id="19dcb-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="19dcb-114">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="19dcb-114">Type: **Integer**</span></span>

<span data-ttu-id="19dcb-115">Valeur **entière** qui spécifie les informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="19dcb-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="19dcb-116">Les informations disponibles pour un élément dépendent du dossier dans lequel il est affiché.</span><span class="sxs-lookup"><span data-stu-id="19dcb-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="19dcb-117">Cette valeur correspond au numéro de colonne de base zéro affiché dans une vue de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="19dcb-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="19dcb-118">Pour un élément dans le système de fichiers, il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="19dcb-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="19dcb-119"> (0)</span><span class="sxs-lookup"><span data-stu-id="19dcb-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="19dcb-120">Récupère le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="19dcb-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="19dcb-121">(1)</span><span class="sxs-lookup"><span data-stu-id="19dcb-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="19dcb-122">Récupère la taille de l’élément.</span><span class="sxs-lookup"><span data-stu-id="19dcb-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="19dcb-123">(2)</span><span class="sxs-lookup"><span data-stu-id="19dcb-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="19dcb-124">Récupère le type de l’élément.</span><span class="sxs-lookup"><span data-stu-id="19dcb-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="19dcb-125">(3)</span><span class="sxs-lookup"><span data-stu-id="19dcb-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="19dcb-126">Récupère la date et l’heure de la dernière modification de l’élément.</span><span class="sxs-lookup"><span data-stu-id="19dcb-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="19dcb-127">(4)</span><span class="sxs-lookup"><span data-stu-id="19dcb-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="19dcb-128">Récupère les attributs de l’élément.</span><span class="sxs-lookup"><span data-stu-id="19dcb-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="19dcb-129">(-1)</span><span class="sxs-lookup"><span data-stu-id="19dcb-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="19dcb-130">Récupère les informations d’info-bulle pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="19dcb-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19dcb-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19dcb-131">Return value</span></span>

<span data-ttu-id="19dcb-132">Type : \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="19dcb-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="19dcb-133">Chaîne contenant le détail récupéré.</span><span class="sxs-lookup"><span data-stu-id="19dcb-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="19dcb-134">Notes</span><span class="sxs-lookup"><span data-stu-id="19dcb-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="19dcb-135">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="19dcb-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="19dcb-136">Par exemple, la méthode [_ *ParseName* \*](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="19dcb-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="19dcb-137">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="19dcb-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="19dcb-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="19dcb-138">Examples</span></span>

<span data-ttu-id="19dcb-139">L’exemple suivant utilise **GetDetailsOf** pour récupérer le type du fichier nommé Clock.avi.</span><span class="sxs-lookup"><span data-stu-id="19dcb-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="19dcb-140">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19dcb-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="19dcb-141">Langage</span><span class="sxs-lookup"><span data-stu-id="19dcb-141">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



<span data-ttu-id="19dcb-142">VBScript</span><span class="sxs-lookup"><span data-stu-id="19dcb-142">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="19dcb-143">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="19dcb-143">Visual Basic:</span></span>


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="19dcb-144">Spécifications</span><span class="sxs-lookup"><span data-stu-id="19dcb-144">Requirements</span></span>



| <span data-ttu-id="19dcb-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19dcb-145">Requirement</span></span> | <span data-ttu-id="19dcb-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="19dcb-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19dcb-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19dcb-147">Minimum supported client</span></span><br/> | <span data-ttu-id="19dcb-148">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19dcb-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="19dcb-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19dcb-149">Minimum supported server</span></span><br/> | <span data-ttu-id="19dcb-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19dcb-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19dcb-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="19dcb-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="19dcb-152"><dt>Shlobj \_ Core. h (include shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19dcb-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="19dcb-153">MIDL</span><span class="sxs-lookup"><span data-stu-id="19dcb-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19dcb-154"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19dcb-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="19dcb-155">DLL</span><span class="sxs-lookup"><span data-stu-id="19dcb-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19dcb-156"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="19dcb-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
