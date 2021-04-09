---
description: La méthode ChangeDir remplace le répertoire de carte à puce actuel par le nouveau répertoire spécifié.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'ISCardFileAccess :: ChangeDir, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862629"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="6b9b7-103">ISCardFileAccess :: ChangeDir, méthode</span><span class="sxs-lookup"><span data-stu-id="6b9b7-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="6b9b7-104">\[La méthode **ChangeDir** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b9b7-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6b9b7-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6b9b7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6b9b7-107">La méthode **ChangeDir** remplace le répertoire de [*carte à puce*](../secgloss/s-gly.md) actuel par le nouveau répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b9b7-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="6b9b7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b9b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9b7-110">*RefType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b9b7-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9b7-111">Type de référence utilisé dans *bstrNewDir*.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="6b9b7-112">**SC \_ type \_ by \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="6b9b7-113">**SC \_ type \_ by \_ ID**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="6b9b7-114">**SC \_ type \_ par \_ short**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="6b9b7-115">**SC \_ type \_ par \_ any**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6b9b7-116">*bstrNewDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b9b7-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9b7-117">Nom de fichier/répertoire (par *RefType*) à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9b7-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b9b7-118">Return value</span></span>

<span data-ttu-id="6b9b7-119">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6b9b7-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6b9b7-120">Return code</span></span>                                                                                   | <span data-ttu-id="6b9b7-121">Description</span><span class="sxs-lookup"><span data-stu-id="6b9b7-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6b9b7-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b9b7-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6b9b7-123">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6b9b7-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6b9b7-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6b9b7-125">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6b9b7-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6b9b7-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6b9b7-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6b9b7-128">Notes</span><span class="sxs-lookup"><span data-stu-id="6b9b7-128">Remarks</span></span>

<span data-ttu-id="6b9b7-129">Pour connaître le chemin d’accès absolu au répertoire actuellement sélectionné, appelez [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span><span class="sxs-lookup"><span data-stu-id="6b9b7-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="6b9b7-130">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="6b9b7-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6b9b7-131">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6b9b7-132">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6b9b7-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9b7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b9b7-133">Requirements</span></span>



| <span data-ttu-id="6b9b7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b9b7-134">Requirement</span></span> | <span data-ttu-id="6b9b7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b9b7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b9b7-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b9b7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6b9b7-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b9b7-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6b9b7-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b9b7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6b9b7-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b9b7-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6b9b7-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6b9b7-140">End of client support</span></span><br/>    | <span data-ttu-id="6b9b7-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b9b7-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6b9b7-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6b9b7-142">End of server support</span></span><br/>    | <span data-ttu-id="6b9b7-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b9b7-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6b9b7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b9b7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b9b7-145">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="6b9b7-146">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
