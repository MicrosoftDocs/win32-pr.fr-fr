---
description: La méthode Close ferme le fichier spécifié. Aucun autre accès au fichier n’est autorisé.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: 'ISCardFileAccess :: Close, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113206"
---
# <a name="iscardfileaccessclose-method"></a><span data-ttu-id="d63ef-104">ISCardFileAccess :: Close, méthode</span><span class="sxs-lookup"><span data-stu-id="d63ef-104">ISCardFileAccess::Close method</span></span>

<span data-ttu-id="d63ef-105">\[La méthode **Close** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d63ef-105">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d63ef-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d63ef-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d63ef-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d63ef-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d63ef-108">La méthode **Close** ferme le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d63ef-108">The **Close** method closes the specified file.</span></span> <span data-ttu-id="d63ef-109">Aucun autre accès au fichier n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="d63ef-109">No further access to file is allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d63ef-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d63ef-110">Syntax</span></span>


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="d63ef-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d63ef-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63ef-112">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d63ef-112">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d63ef-113">Handle du fichier à fermer.</span><span class="sxs-lookup"><span data-stu-id="d63ef-113">A handle to the file to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d63ef-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d63ef-114">Return value</span></span>

<span data-ttu-id="d63ef-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="d63ef-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d63ef-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d63ef-116">Return code</span></span>                                                                                   | <span data-ttu-id="d63ef-117">Description</span><span class="sxs-lookup"><span data-stu-id="d63ef-117">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d63ef-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d63ef-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d63ef-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d63ef-119">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d63ef-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d63ef-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d63ef-121">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="d63ef-121">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="d63ef-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d63ef-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d63ef-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d63ef-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d63ef-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d63ef-124">Remarks</span></span>

<span data-ttu-id="d63ef-125">Pour ouvrir un fichier, appelez [**Open**](iscardfileaccess-open.md).</span><span class="sxs-lookup"><span data-stu-id="d63ef-125">To open a file, call [**Open**](iscardfileaccess-open.md).</span></span>

<span data-ttu-id="d63ef-126">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="d63ef-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="d63ef-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="d63ef-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d63ef-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d63ef-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d63ef-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d63ef-129">Requirements</span></span>



| <span data-ttu-id="d63ef-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d63ef-130">Requirement</span></span> | <span data-ttu-id="d63ef-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d63ef-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d63ef-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d63ef-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d63ef-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d63ef-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d63ef-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d63ef-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d63ef-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d63ef-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d63ef-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d63ef-136">End of client support</span></span><br/>    | <span data-ttu-id="d63ef-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d63ef-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d63ef-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d63ef-138">End of server support</span></span><br/>    | <span data-ttu-id="d63ef-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d63ef-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d63ef-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d63ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63ef-141">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="d63ef-141">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="d63ef-142">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="d63ef-142">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
