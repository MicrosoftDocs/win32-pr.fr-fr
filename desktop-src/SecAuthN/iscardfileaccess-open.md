---
description: La méthode Open ouvre le fichier spécifié pour une utilisation ultérieure.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'ISCardFileAccess :: Open, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115339"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="c5adf-103">ISCardFileAccess :: Open, méthode</span><span class="sxs-lookup"><span data-stu-id="c5adf-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="c5adf-104">\[La méthode **Open** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c5adf-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5adf-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c5adf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c5adf-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="c5adf-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c5adf-107">La méthode **Open** ouvre le fichier spécifié pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c5adf-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5adf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5adf-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="c5adf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5adf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5adf-110">*RefType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5adf-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adf-111">Type de référence utilisé dans *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="c5adf-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="c5adf-112">**SC \_ type \_ by \_ Name**</span><span class="sxs-lookup"><span data-stu-id="c5adf-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="c5adf-113">**SC \_ type \_ by \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c5adf-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="c5adf-114">**SC \_ type \_ par \_ short**</span><span class="sxs-lookup"><span data-stu-id="c5adf-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="c5adf-115">**SC \_ type \_ par \_ any**</span><span class="sxs-lookup"><span data-stu-id="c5adf-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="c5adf-116">*bstrPathSpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5adf-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adf-117">Fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="c5adf-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="c5adf-118">*phFile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c5adf-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adf-119">Pointeur vers un fichier HSCARD qui contiendra \_ le descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="c5adf-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5adf-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5adf-120">Return value</span></span>

<span data-ttu-id="c5adf-121">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5adf-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c5adf-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c5adf-122">Return code</span></span>                                                                                   | <span data-ttu-id="c5adf-123">Description</span><span class="sxs-lookup"><span data-stu-id="c5adf-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c5adf-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5adf-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c5adf-125">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c5adf-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c5adf-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c5adf-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c5adf-127">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="c5adf-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c5adf-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c5adf-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c5adf-129">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="c5adf-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c5adf-130"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="c5adf-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c5adf-131">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="c5adf-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c5adf-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c5adf-132">Remarks</span></span>

<span data-ttu-id="c5adf-133">Pour fermer un fichier, appelez [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="c5adf-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="c5adf-134">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="c5adf-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="c5adf-135">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="c5adf-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c5adf-136">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c5adf-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5adf-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5adf-137">Requirements</span></span>



| <span data-ttu-id="c5adf-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5adf-138">Requirement</span></span> | <span data-ttu-id="c5adf-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5adf-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5adf-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5adf-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c5adf-141">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5adf-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c5adf-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5adf-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c5adf-143">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5adf-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c5adf-144">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c5adf-144">End of client support</span></span><br/>    | <span data-ttu-id="c5adf-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5adf-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c5adf-146">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c5adf-146">End of server support</span></span><br/>    | <span data-ttu-id="c5adf-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5adf-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c5adf-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5adf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5adf-149">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="c5adf-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="c5adf-150">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="c5adf-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
