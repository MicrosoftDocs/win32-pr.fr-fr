---
description: La méthode Delete supprime un fichier à un emplacement donné au sein du système de fichiers de la carte à puce.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: ISCardFileAccess ::D méthode supprimable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318417"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="4398b-103">ISCardFileAccess ::D méthode supprimable</span><span class="sxs-lookup"><span data-stu-id="4398b-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="4398b-104">\[La méthode de **suppression** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="4398b-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4398b-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4398b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4398b-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4398b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4398b-107">La méthode **Delete** supprime un fichier à un emplacement donné au sein du système de fichiers de la [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4398b-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4398b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4398b-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="4398b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4398b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4398b-110">*RefType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4398b-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4398b-111">Type de référence utilisé dans *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="4398b-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="4398b-112">**SC \_ type \_ by \_ Name**</span><span class="sxs-lookup"><span data-stu-id="4398b-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="4398b-113">**SC \_ type \_ by \_ ID**</span><span class="sxs-lookup"><span data-stu-id="4398b-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="4398b-114">**SC \_ type \_ par \_ short**</span><span class="sxs-lookup"><span data-stu-id="4398b-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="4398b-115">**SC \_ type \_ par \_ any**</span><span class="sxs-lookup"><span data-stu-id="4398b-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4398b-116">*bstrPathSpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4398b-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4398b-117">Identificateur du fichier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4398b-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="4398b-118">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4398b-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4398b-119">Spécifie si la messagerie sécurisée doit être utilisée et les données préallouées.</span><span class="sxs-lookup"><span data-stu-id="4398b-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="4398b-120">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="4398b-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="4398b-121">**SC \_ FL \_ préalloué**</span><span class="sxs-lookup"><span data-stu-id="4398b-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4398b-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4398b-122">Return value</span></span>

<span data-ttu-id="4398b-123">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="4398b-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4398b-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4398b-124">Return code</span></span>                                                                                  | <span data-ttu-id="4398b-125">Description</span><span class="sxs-lookup"><span data-stu-id="4398b-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="4398b-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4398b-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4398b-127">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4398b-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="4398b-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4398b-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4398b-129">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4398b-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="4398b-130"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="4398b-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="4398b-131">L’interface n’a pas implémenté cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4398b-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4398b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="4398b-132">Remarks</span></span>

<span data-ttu-id="4398b-133">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="4398b-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="4398b-134">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="4398b-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4398b-135">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4398b-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4398b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4398b-136">Requirements</span></span>



| <span data-ttu-id="4398b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4398b-137">Requirement</span></span> | <span data-ttu-id="4398b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4398b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4398b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4398b-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4398b-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4398b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4398b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4398b-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4398b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4398b-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4398b-143">End of client support</span></span><br/>    | <span data-ttu-id="4398b-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4398b-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4398b-145">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4398b-145">End of server support</span></span><br/>    | <span data-ttu-id="4398b-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4398b-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4398b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4398b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4398b-148">**Créés**</span><span class="sxs-lookup"><span data-stu-id="4398b-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="4398b-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="4398b-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
