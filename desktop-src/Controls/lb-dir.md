---
title: Message LB_DIR (winuser. h)
description: Ajoute des noms à la liste affichée par une zone de liste. Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier. LB \_ dir peut également ajouter des lettres de lecteur mappées à la zone de liste.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106000"
---
# <a name="lb_dir-message"></a><span data-ttu-id="1829d-106">Message du répertoire du LB \_</span><span class="sxs-lookup"><span data-stu-id="1829d-106">LB\_DIR message</span></span>

<span data-ttu-id="1829d-107">Ajoute des noms à la liste affichée par une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="1829d-108">Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="1829d-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="1829d-109">**Lb \_ DIR** peut également ajouter des lettres de lecteur mappées à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1829d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1829d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1829d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1829d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1829d-112">Attributs des fichiers ou répertoires à ajouter à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="1829d-113">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1829d-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1829d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1829d-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="1829d-115">Signification</span><span class="sxs-lookup"><span data-stu-id="1829d-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="1829d-116"><dt>**\_Archive DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="1829d-117">Comprend les fichiers archivés.</span><span class="sxs-lookup"><span data-stu-id="1829d-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="1829d-118"><dt>**\_répertoire DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="1829d-119">Comprend des sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="1829d-119">Includes subdirectories.</span></span> <span data-ttu-id="1829d-120">Les noms de sous-répertoires sont placés entre crochets ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="1829d-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="1829d-121"><dt>**\_lecteurs DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="1829d-122">Tous les lecteurs mappés sont ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="1829d-123">Les lecteurs sont répertoriés sous la forme \[ - *x* - \] , où *x* est la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="1829d-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="1829d-124"><dt>**DLL en \_ mode exclusif**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="1829d-125">Comprend uniquement les fichiers avec les attributs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1829d-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="1829d-126">Par défaut, les fichiers en lecture/écriture sont répertoriés même si DDL \_ ReadWrite n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="1829d-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="1829d-127"><dt>**DDL \_ masqué**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="1829d-128">Comprend les fichiers masqués.</span><span class="sxs-lookup"><span data-stu-id="1829d-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="1829d-129"><dt>**DDL \_ ReadOnly**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="1829d-130">Comprend des fichiers en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1829d-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="1829d-131"><dt>**lecture/ \_ écriture DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="1829d-132">Comprend des fichiers en lecture/écriture sans attributs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1829d-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="1829d-133">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="1829d-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="1829d-134"><dt>**\_système DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="1829d-135">Comprend des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="1829d-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="1829d-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1829d-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1829d-137">Pointeur vers la chaîne terminée par le caractère null qui spécifie un chemin d’accès absolu, un chemin d’accès relatif ou un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1829d-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="1829d-138">Un chemin d’accès absolu peut commencer par une lettre de lecteur (par exemple, d : \) ou un nom UNC (par exemple, \\ \\ *MachineName* \\ *Nom_Partage*).</span><span class="sxs-lookup"><span data-stu-id="1829d-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="1829d-139">Si la chaîne spécifie un nom de fichier ou un répertoire qui a les attributs spécifiés par le paramètre *wParam* , le nom de fichier ou le répertoire est ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="1829d-140">Si le nom de fichier ou de répertoire contient des caractères génériques ( ?</span><span class="sxs-lookup"><span data-stu-id="1829d-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="1829d-141">ou \* ), tous les fichiers ou répertoires qui correspondent à l’expression générique et dont les attributs sont spécifiés par le paramètre *wParam* sont ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1829d-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1829d-142">Return value</span></span>

<span data-ttu-id="1829d-143">Si le message est correctement exécuté, la valeur de retour est l’index de base zéro du dernier nom ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="1829d-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="1829d-144">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="1829d-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="1829d-145">Si l’espace est insuffisant pour stocker les nouvelles chaînes, la valeur de retour est LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="1829d-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1829d-146">Notes</span><span class="sxs-lookup"><span data-stu-id="1829d-146">Remarks</span></span>

<span data-ttu-id="1829d-147">Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100).</span><span class="sxs-lookup"><span data-stu-id="1829d-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="1829d-148">Il réserve la quantité de mémoire spécifiée afin que les messages de **\_ Répertoire de livres** suivants prennent le plus de temps possible.</span><span class="sxs-lookup"><span data-stu-id="1829d-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="1829d-149">Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1829d-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="1829d-150">Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.</span><span class="sxs-lookup"><span data-stu-id="1829d-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="1829d-151">Si *wParam* inclut l' \_ indicateur de répertoire DDL et que *lParam* spécifie tous les sous-répertoires d’un répertoire de premier niveau, par exemple C : \\ temp \\ \* , la zone de liste inclura toujours une entrée « .. » pour le répertoire racine.</span><span class="sxs-lookup"><span data-stu-id="1829d-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="1829d-152">Cela est vrai même si le répertoire racine contient des attributs système ou masqués et que les \_ indicateurs système DDL et DDL ne \_ sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1829d-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="1829d-153">Le répertoire racine d’un volume NTFS a des attributs système et masqués.</span><span class="sxs-lookup"><span data-stu-id="1829d-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="1829d-154">La liste affiche les noms de fichiers longs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1829d-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="1829d-155">Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="1829d-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="1829d-156">Cela peut entraîner des problèmes.</span><span class="sxs-lookup"><span data-stu-id="1829d-156">This can cause problems.</span></span> <span data-ttu-id="1829d-157">Par exemple, les caractères romains accentués dans une zone de liste non Unicode dans les fenêtres japonaises sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="1829d-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="1829d-158">Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="1829d-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1829d-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1829d-159">Requirements</span></span>



| <span data-ttu-id="1829d-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1829d-160">Requirement</span></span> | <span data-ttu-id="1829d-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="1829d-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1829d-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1829d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1829d-163">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1829d-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1829d-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1829d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1829d-165">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1829d-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1829d-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="1829d-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="1829d-167"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1829d-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1829d-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1829d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1829d-169">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="1829d-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





