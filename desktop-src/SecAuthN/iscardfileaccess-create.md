---
description: La méthode Create crée un fichier à un emplacement donné au sein du système de fichiers de la carte à puce.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'ISCardFileAccess :: Create, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113202"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="ace39-103">ISCardFileAccess :: Create, méthode</span><span class="sxs-lookup"><span data-stu-id="ace39-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="ace39-104">\[La méthode **Create** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ace39-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ace39-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ace39-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ace39-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ace39-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ace39-107">La méthode **Create** crée un fichier à un emplacement donné au sein du système de fichiers de la [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ace39-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace39-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ace39-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ace39-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ace39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace39-110">*RefType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace39-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace39-111">Type de référence utilisé dans *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="ace39-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="ace39-112">**SC \_ type \_ by \_ Name**</span><span class="sxs-lookup"><span data-stu-id="ace39-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="ace39-113">**SC \_ type \_ by \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ace39-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="ace39-114">**SC \_ type \_ par \_ short**</span><span class="sxs-lookup"><span data-stu-id="ace39-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="ace39-115">**SC \_ type \_ par \_ any**</span><span class="sxs-lookup"><span data-stu-id="ace39-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="ace39-116">*bstrPathSpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace39-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace39-117">ID de fichier à créer dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="ace39-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="ace39-118">*TLV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace39-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace39-119">Liste des structures TLV (tag, Length, value) dont les valeurs doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="ace39-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="ace39-120">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace39-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace39-121">Spécifie si la messagerie sécurisée doit être utilisée et les données préallouées.</span><span class="sxs-lookup"><span data-stu-id="ace39-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="ace39-122">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="ace39-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="ace39-123">**SC \_ FL \_ préalloué**</span><span class="sxs-lookup"><span data-stu-id="ace39-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="ace39-124">*pDataBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace39-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace39-125">Pointeur vers des données préallouées.</span><span class="sxs-lookup"><span data-stu-id="ace39-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace39-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ace39-126">Return value</span></span>

<span data-ttu-id="ace39-127">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="ace39-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ace39-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ace39-128">Return code</span></span>                                                                                   | <span data-ttu-id="ace39-129">Description</span><span class="sxs-lookup"><span data-stu-id="ace39-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ace39-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ace39-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ace39-131">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ace39-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ace39-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ace39-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ace39-133">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="ace39-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="ace39-134"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ace39-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ace39-135">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="ace39-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="ace39-136"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ace39-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ace39-137">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ace39-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ace39-138">Notes</span><span class="sxs-lookup"><span data-stu-id="ace39-138">Remarks</span></span>

<span data-ttu-id="ace39-139">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="ace39-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="ace39-140">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="ace39-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ace39-141">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ace39-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ace39-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ace39-142">Requirements</span></span>



| <span data-ttu-id="ace39-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ace39-143">Requirement</span></span> | <span data-ttu-id="ace39-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="ace39-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ace39-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace39-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ace39-146">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ace39-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ace39-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace39-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ace39-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ace39-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ace39-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ace39-149">End of client support</span></span><br/>    | <span data-ttu-id="ace39-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ace39-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="ace39-151">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ace39-151">End of server support</span></span><br/>    | <span data-ttu-id="ace39-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ace39-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="ace39-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ace39-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace39-154">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="ace39-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
