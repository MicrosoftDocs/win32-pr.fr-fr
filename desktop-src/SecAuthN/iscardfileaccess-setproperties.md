---
description: La méthode SetProperties définit la primitive référencée par TLVs (balise, longueur, valeur) pour l’objet spécifié.
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: 'ISCardFileAccess :: SetProperties, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544806"
---
# <a name="iscardfileaccesssetproperties-method"></a><span data-ttu-id="6d201-103">ISCardFileAccess :: SetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="6d201-103">ISCardFileAccess::SetProperties method</span></span>

<span data-ttu-id="6d201-104">\[La méthode **SetProperties** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6d201-104">\[The **SetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d201-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6d201-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6d201-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6d201-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6d201-107">La méthode **SetProperties** définit la primitive référencée par TLVs (balise, longueur, valeur) pour l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="6d201-107">The **SetProperties** method sets the primitive referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d201-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d201-108">Syntax</span></span>


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
);
```



## <a name="parameters"></a><span data-ttu-id="6d201-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d201-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d201-110">*RefType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d201-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d201-111">Type de référence utilisé dans *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="6d201-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="6d201-112">**SC \_ type \_ by \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6d201-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="6d201-113">**SC \_ type \_ by \_ ID**</span><span class="sxs-lookup"><span data-stu-id="6d201-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="6d201-114">**SC \_ type \_ par \_ short**</span><span class="sxs-lookup"><span data-stu-id="6d201-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="6d201-115">**SC \_ type \_ par \_ any**</span><span class="sxs-lookup"><span data-stu-id="6d201-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6d201-116">*bstrPathSpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d201-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d201-117">Fichier.</span><span class="sxs-lookup"><span data-stu-id="6d201-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="6d201-118">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d201-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d201-119">Spécifie si la messagerie sécurisée doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6d201-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="6d201-120">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="6d201-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6d201-121">*pTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d201-121">*pTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d201-122">Pointeur vers les structures TLV dont la valeur doit être définie.</span><span class="sxs-lookup"><span data-stu-id="6d201-122">Pointer to TLV structures whose value should be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d201-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d201-123">Return value</span></span>

<span data-ttu-id="6d201-124">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d201-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6d201-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6d201-125">Return code</span></span>                                                                                   | <span data-ttu-id="6d201-126">Description</span><span class="sxs-lookup"><span data-stu-id="6d201-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6d201-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d201-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6d201-128">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6d201-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6d201-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6d201-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6d201-130">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="6d201-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6d201-131"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="6d201-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6d201-132">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="6d201-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6d201-133"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6d201-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6d201-134">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6d201-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6d201-135">Notes</span><span class="sxs-lookup"><span data-stu-id="6d201-135">Remarks</span></span>

<span data-ttu-id="6d201-136">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="6d201-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6d201-137">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="6d201-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6d201-138">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6d201-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d201-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d201-139">Requirements</span></span>



| <span data-ttu-id="6d201-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d201-140">Requirement</span></span> | <span data-ttu-id="6d201-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d201-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6d201-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d201-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6d201-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d201-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6d201-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d201-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6d201-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d201-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6d201-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6d201-146">End of client support</span></span><br/>    | <span data-ttu-id="6d201-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d201-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6d201-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6d201-148">End of server support</span></span><br/>    | <span data-ttu-id="6d201-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d201-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6d201-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d201-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d201-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="6d201-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
