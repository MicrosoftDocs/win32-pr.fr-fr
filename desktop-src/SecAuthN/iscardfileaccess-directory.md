---
description: La méthode Directory récupère une liste de fichiers du type spécifié dans le répertoire actif.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess ::D méthode ire
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864049"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="d2189-103">ISCardFileAccess ::D méthode ire</span><span class="sxs-lookup"><span data-stu-id="d2189-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="d2189-104">\[La méthode d' **Annuaire** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d2189-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d2189-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d2189-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d2189-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d2189-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d2189-107">La méthode **Directory** récupère une liste de fichiers du type spécifié dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="d2189-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2189-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2189-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="d2189-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2189-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2189-110">*filetype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2189-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2189-111">Type de fichiers de [*carte à puce*](../secgloss/s-gly.md) à répertorier.</span><span class="sxs-lookup"><span data-stu-id="d2189-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="d2189-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2189-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="d2189-113">Signification</span><span class="sxs-lookup"><span data-stu-id="d2189-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="d2189-114"><dt>**\_répertoires de type SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="d2189-115">Répertorier uniquement les fichiers du répertoire.</span><span class="sxs-lookup"><span data-stu-id="d2189-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="d2189-116"><dt>**\_fichiers de type SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="d2189-117">Répertorier uniquement les fichiers élémentaires.</span><span class="sxs-lookup"><span data-stu-id="d2189-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="d2189-118"><dt>**SC- \_ type \_ tous les \_ fichiers**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="d2189-119">Répertoriez à la fois le répertoire et les fichiers élémentaires.</span><span class="sxs-lookup"><span data-stu-id="d2189-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="d2189-120"><dt>**\_fichier de \_ Répertoire de type SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="d2189-121">Fichier de répertoire.</span><span class="sxs-lookup"><span data-stu-id="d2189-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="d2189-122"><dt>**\_type SC \_ transparent \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="d2189-123">Fichier élémentaire transparent.</span><span class="sxs-lookup"><span data-stu-id="d2189-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="d2189-124"><dt>**\_type SC \_ fixe \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="d2189-125">Fichier élémentaire fixe linéaire.</span><span class="sxs-lookup"><span data-stu-id="d2189-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="d2189-126"><dt>**SC \_ type \_ \_ EF cyclique**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="d2189-127">Fichier élémentaire cyclique.</span><span class="sxs-lookup"><span data-stu-id="d2189-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="d2189-128"><dt>**\_variable de type SC \_ \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="d2189-129">Fichier élémentaire de variable linéaire.</span><span class="sxs-lookup"><span data-stu-id="d2189-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="d2189-130">*ppFileList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d2189-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2189-131">Tableau de BSTR représentant la liste des fichiers correspondant au spécificateur dans *filetype*.</span><span class="sxs-lookup"><span data-stu-id="d2189-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2189-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2189-132">Return value</span></span>

<span data-ttu-id="d2189-133">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2189-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d2189-134">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d2189-134">Return code</span></span>                                                                                   | <span data-ttu-id="d2189-135">Description</span><span class="sxs-lookup"><span data-stu-id="d2189-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="d2189-136"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d2189-137">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d2189-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="d2189-138"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d2189-139">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="d2189-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="d2189-140"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d2189-141">L’interface n’a pas implémenté cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d2189-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="d2189-142"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d2189-143">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d2189-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d2189-144"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d2189-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d2189-145">Un pointeur incorrect a été transmis pour *ppFileList*.</span><span class="sxs-lookup"><span data-stu-id="d2189-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d2189-146">Notes</span><span class="sxs-lookup"><span data-stu-id="d2189-146">Remarks</span></span>

<span data-ttu-id="d2189-147">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="d2189-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="d2189-148">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="d2189-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d2189-149">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d2189-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2189-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2189-150">Requirements</span></span>



| <span data-ttu-id="d2189-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2189-151">Requirement</span></span> | <span data-ttu-id="d2189-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2189-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2189-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2189-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d2189-154">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2189-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d2189-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2189-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d2189-156">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2189-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2189-157">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d2189-157">End of client support</span></span><br/>    | <span data-ttu-id="d2189-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2189-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d2189-159">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d2189-159">End of server support</span></span><br/>    | <span data-ttu-id="d2189-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2189-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d2189-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2189-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2189-162">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="d2189-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
