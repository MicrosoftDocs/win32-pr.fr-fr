---
title: Message CB_DIR (winuser. h)
description: Ajoute des noms à la liste affichée par la zone de liste déroulante. Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier. \_Le répertoire CB peut également ajouter des lettres de lecteur mappées à la liste.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843577"
---
# <a name="cb_dir-message"></a><span data-ttu-id="01a4f-106">\_Message du répertoire CB</span><span class="sxs-lookup"><span data-stu-id="01a4f-106">CB\_DIR message</span></span>

<span data-ttu-id="01a4f-107">Ajoute des noms à la liste affichée par la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="01a4f-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="01a4f-108">Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="01a4f-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="01a4f-109">**CB \_ DIR** peut également ajouter des lettres de lecteur mappées à la liste.</span><span class="sxs-lookup"><span data-stu-id="01a4f-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="01a4f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01a4f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a4f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01a4f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01a4f-112">Attributs des fichiers ou répertoires à ajouter à la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="01a4f-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="01a4f-113">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="01a4f-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="01a4f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="01a4f-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="01a4f-115">Signification</span><span class="sxs-lookup"><span data-stu-id="01a4f-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="01a4f-116"><dt>**\_Archive DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="01a4f-117">Comprend les fichiers archivés.</span><span class="sxs-lookup"><span data-stu-id="01a4f-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="01a4f-118"><dt>**\_répertoire DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="01a4f-119">Comprend les sous-répertoires, qui sont placés entre crochets ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="01a4f-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="01a4f-120"><dt>**\_lecteurs DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="01a4f-121">Tous les lecteurs mappés sont ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="01a4f-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="01a4f-122">Les lecteurs sont répertoriés sous la forme \[ - *x* - \] , où *x* est la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="01a4f-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="01a4f-123"><dt>**DLL en \_ mode exclusif**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="01a4f-124">Comprend uniquement les fichiers avec les attributs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="01a4f-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="01a4f-125">Par défaut, les fichiers en lecture/écriture sont répertoriés même si DDL \_ ReadWrite n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="01a4f-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="01a4f-126"><dt>**DDL \_ masqué**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="01a4f-127">Comprend les fichiers masqués.</span><span class="sxs-lookup"><span data-stu-id="01a4f-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="01a4f-128"><dt>**DDL \_ ReadOnly**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="01a4f-129">Comprend des fichiers en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="01a4f-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="01a4f-130"><dt>**lecture/ \_ écriture DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="01a4f-131">Comprend des fichiers en lecture/écriture sans attributs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="01a4f-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="01a4f-132">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="01a4f-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="01a4f-133"><dt>**\_système DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="01a4f-134">Comprend des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="01a4f-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="01a4f-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01a4f-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01a4f-136">Pointeur **LPCTSTR** vers une chaîne se terminant par un caractère null qui spécifie un chemin d’accès absolu, un chemin d’accès relatif ou un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="01a4f-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="01a4f-137">Un chemin d’accès absolu peut commencer par une lettre de lecteur (par exemple, d : \) ou un nom UNC (par exemple, \\ \\ *MachineName* \\ *Nom_Partage*).</span><span class="sxs-lookup"><span data-stu-id="01a4f-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="01a4f-138">Si la chaîne spécifie un nom de fichier ou un répertoire qui a les attributs spécifiés par le paramètre *wParam* , le nom de fichier ou le répertoire est ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="01a4f-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="01a4f-139">Si le nom de fichier ou le nom de répertoire contient des caractères génériques ( ?</span><span class="sxs-lookup"><span data-stu-id="01a4f-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="01a4f-140">ou \* ), tous les fichiers ou répertoires qui correspondent à l’expression générique et dont les attributs sont spécifiés par le paramètre *wParam* sont ajoutés à la liste affichée dans la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="01a4f-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a4f-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01a4f-141">Return value</span></span>

<span data-ttu-id="01a4f-142">Si le message est correctement exécuté, la valeur de retour est l’index de base zéro du dernier nom ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="01a4f-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="01a4f-143">Si une erreur se produit, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="01a4f-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="01a4f-144">Si l’espace est insuffisant pour stocker les nouvelles chaînes, la valeur de retour est CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="01a4f-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a4f-145">Notes</span><span class="sxs-lookup"><span data-stu-id="01a4f-145">Remarks</span></span>

<span data-ttu-id="01a4f-146">Si *wParam* inclut l' \_ indicateur de répertoire DDL et que *lParam* spécifie tous les sous-répertoires d’un répertoire de premier niveau, par exemple C : \\ temp \\ \* , la zone de liste inclura toujours une entrée « .. » pour le répertoire racine.</span><span class="sxs-lookup"><span data-stu-id="01a4f-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="01a4f-147">Cela est vrai même si le répertoire racine contient des attributs système ou masqués et que les \_ indicateurs système DDL et DDL ne \_ sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="01a4f-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="01a4f-148">Le répertoire racine d’un volume NTFS a des attributs système et masqués.</span><span class="sxs-lookup"><span data-stu-id="01a4f-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="01a4f-149">La liste affiche les noms de fichiers longs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="01a4f-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a4f-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01a4f-150">Requirements</span></span>



| <span data-ttu-id="01a4f-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01a4f-151">Requirement</span></span> | <span data-ttu-id="01a4f-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="01a4f-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a4f-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a4f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="01a4f-154">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01a4f-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01a4f-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a4f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="01a4f-156">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01a4f-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01a4f-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="01a4f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a4f-158"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01a4f-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a4f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01a4f-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="01a4f-160">**Référence**</span><span class="sxs-lookup"><span data-stu-id="01a4f-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01a4f-161">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="01a4f-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="01a4f-162">**\_INSERTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="01a4f-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="01a4f-163">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="01a4f-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





