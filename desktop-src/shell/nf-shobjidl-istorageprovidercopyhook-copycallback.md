---
description: Détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104991841"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="e6e02-103">IStorageProviderCopyHook :: CopyCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="e6e02-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="e6e02-104">Détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.</span><span class="sxs-lookup"><span data-stu-id="e6e02-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6e02-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="e6e02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6e02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e02-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-108">Handle de la fenêtre que le gestionnaire de raccordement de copie doit utiliser comme parent pour tous les éléments d’interface utilisateur que le gestionnaire peut avoir besoin d’afficher.</span><span class="sxs-lookup"><span data-stu-id="e6e02-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="e6e02-109">Si **FOF_SILENT** est spécifié dans l' *opération*, la méthode doit ignorer ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6e02-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="e6e02-110">*opération* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-111">Opération à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e6e02-111">The operation to perform.</span></span> <span data-ttu-id="e6e02-112">Ce paramètre peut être l’une des valeurs listées sous le membre **wFunc** de la structure [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="e6e02-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="e6e02-113">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-114">Indicateurs qui contrôlent l’opération.</span><span class="sxs-lookup"><span data-stu-id="e6e02-114">The flags that control the operation.</span></span> <span data-ttu-id="e6e02-115">Ce paramètre peut être une ou plusieurs des valeurs listées sous le membre *fFlags* de la structure [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="e6e02-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="e6e02-116">Pour les raccordements de copie d’imprimante, cette valeur est l’une des valeurs suivantes définies dans shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="e6e02-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="e6e02-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6e02-117">Value</span></span>       | <span data-ttu-id="e6e02-118">Description</span><span class="sxs-lookup"><span data-stu-id="e6e02-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="e6e02-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="e6e02-119">**PO_DELETE**</span></span>      | <span data-ttu-id="e6e02-120">Une imprimante est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="e6e02-120">A printer is being deleted.</span></span> <span data-ttu-id="e6e02-121">Le paramètre *srcFile* pointe vers le chemin d’accès complet à l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e6e02-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="e6e02-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="e6e02-122">**PO_RENAME**</span></span>       | <span data-ttu-id="e6e02-123">Une imprimante est renommée.</span><span class="sxs-lookup"><span data-stu-id="e6e02-123">A printer is being renamed.</span></span> <span data-ttu-id="e6e02-124">Le paramètre *srcFile* pointe vers le nouveau nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="e6e02-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="e6e02-125">Le paramètre *destFile* pointe vers l’ancien nom.</span><span class="sxs-lookup"><span data-stu-id="e6e02-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="e6e02-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="e6e02-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="e6e02-127">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6e02-127">Not supported.</span></span> <span data-ttu-id="e6e02-128">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="e6e02-128">Do not use.</span></span>          |
| <span data-ttu-id="e6e02-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="e6e02-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="e6e02-130">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6e02-130">Not supported.</span></span> <span data-ttu-id="e6e02-131">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="e6e02-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="e6e02-132">*srcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-133">Pointeur vers une chaîne qui contient le nom du dossier source.</span><span class="sxs-lookup"><span data-stu-id="e6e02-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="e6e02-134">*srcAttribs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-135">Attributs du dossier source.</span><span class="sxs-lookup"><span data-stu-id="e6e02-135">The attributes of the source folder.</span></span> <span data-ttu-id="e6e02-136">Ce paramètre peut être une combinaison de l’un des indicateurs d’attribut de fichier (FILE_ATTRIBUTE_ \*) définis dans les fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e6e02-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="e6e02-137">Consultez [constantes d’attribut de fichier](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e6e02-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="e6e02-138">*destFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-139">Pointeur vers une chaîne qui contient le nom du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="e6e02-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="e6e02-140">*destAttribs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-141">Attributs du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="e6e02-141">The attributes of the destination folder.</span></span> <span data-ttu-id="e6e02-142">Ce paramètre peut être une combinaison de l’un des indicateurs d’attribut de fichier (FILE_ATTRIBUTE_ \*) définis dans les fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e6e02-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="e6e02-143">Consultez [constantes d’attribut de fichier](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e6e02-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="e6e02-144">*résultat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6e02-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e02-145">Valeur entière qui indique si l’interpréteur de commandes doit effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e6e02-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="e6e02-146">Celui-ci peut avoir l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6e02-146">One of the following:</span></span>

| <span data-ttu-id="e6e02-147">Value</span><span class="sxs-lookup"><span data-stu-id="e6e02-147">Value</span></span>       | <span data-ttu-id="e6e02-148">Description</span><span class="sxs-lookup"><span data-stu-id="e6e02-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="e6e02-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="e6e02-149">**IDYES**</span></span>       | <span data-ttu-id="e6e02-150">Autorise l’opération.</span><span class="sxs-lookup"><span data-stu-id="e6e02-150">Allows the operation.</span></span>           |
| <span data-ttu-id="e6e02-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="e6e02-151">**IDNO**</span></span>        | <span data-ttu-id="e6e02-152">Empêche l’opération sur ce dossier, mais continue avec les autres opérations qui ont été approuvées (par exemple, une opération de copie par lot).</span><span class="sxs-lookup"><span data-stu-id="e6e02-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="e6e02-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="e6e02-153">**IDCANCEL**</span></span>    | <span data-ttu-id="e6e02-154">Empêche l’opération en cours et annule toutes les opérations en attente.</span><span class="sxs-lookup"><span data-stu-id="e6e02-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="e6e02-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6e02-155">Return value</span></span>

<span data-ttu-id="e6e02-156">Retourne **S_OK** en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e6e02-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e02-157">Notes</span><span class="sxs-lookup"><span data-stu-id="e6e02-157">Remarks</span></span>

<span data-ttu-id="e6e02-158">L’interpréteur de commandes appelle le gestionnaire de raccordement de copie du fournisseur de Cloud pour chaque dossier sous la racine de synchronisation inscrite.</span><span class="sxs-lookup"><span data-stu-id="e6e02-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="e6e02-159">Pour inscrire un gestionnaire de raccordement de copie pour les dossiers Cloud, définissez la valeur **CopyHook** sous la clé **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SYNCROOTMANAGER/{SYNCROOTID}** sur le CLSID de l’objet de raccordement de copie.</span><span class="sxs-lookup"><span data-stu-id="e6e02-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="e6e02-160">Lorsque la méthode **CopyCallback** est appelée, l’interpréteur de commandes Initialise l’interface [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) directement sans utiliser d’abord une interface [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .</span><span class="sxs-lookup"><span data-stu-id="e6e02-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e02-161">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e6e02-161">Requirements</span></span>

| <span data-ttu-id="e6e02-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6e02-162">Requirement</span></span> | <span data-ttu-id="e6e02-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6e02-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e02-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6e02-164">Minimum supported client</span></span> | <span data-ttu-id="e6e02-165">Windows 10 Insider Preview, version 19624</span><span class="sxs-lookup"><span data-stu-id="e6e02-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="e6e02-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6e02-166">Header</span></span>                   | <span data-ttu-id="e6e02-167">ShObjIdl. h</span><span class="sxs-lookup"><span data-stu-id="e6e02-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="e6e02-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6e02-168">See also</span></span>

[<span data-ttu-id="e6e02-169">Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé</span><span class="sxs-lookup"><span data-stu-id="e6e02-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)