---
description: La méthode Write écrit des données dans un fichier ouvert en cours.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: 'ISCardFileAccess :: Write, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115338"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="31530-103">ISCardFileAccess :: Write, méthode</span><span class="sxs-lookup"><span data-stu-id="31530-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="31530-104">\[La méthode **Write** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="31530-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31530-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="31530-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="31530-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="31530-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="31530-107">La méthode **Write** écrit des données dans un fichier ouvert en cours.</span><span class="sxs-lookup"><span data-stu-id="31530-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="31530-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31530-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="31530-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31530-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31530-110">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31530-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31530-111">Handle d’un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="31530-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="31530-112">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31530-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31530-113">Objet/données à écrire.</span><span class="sxs-lookup"><span data-stu-id="31530-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="31530-114">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31530-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31530-115">Spécifie si la messagerie sécurisée doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="31530-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="31530-116">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="31530-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31530-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31530-117">Return value</span></span>

<span data-ttu-id="31530-118">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="31530-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="31530-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="31530-119">Return code</span></span>                                                                                   | <span data-ttu-id="31530-120">Description</span><span class="sxs-lookup"><span data-stu-id="31530-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="31530-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31530-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="31530-122">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="31530-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="31530-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="31530-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="31530-124">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="31530-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="31530-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="31530-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="31530-126">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="31530-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="31530-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="31530-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="31530-128">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="31530-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="31530-129">Notes</span><span class="sxs-lookup"><span data-stu-id="31530-129">Remarks</span></span>

<span data-ttu-id="31530-130">Pour ouvrir ou fermer un fichier, appelez [**ouvrir**](iscardfileaccess-open.md) ou [**Fermer**](iscardfileaccess-close.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="31530-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="31530-131">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="31530-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="31530-132">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="31530-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="31530-133">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="31530-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31530-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31530-134">Requirements</span></span>



| <span data-ttu-id="31530-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31530-135">Requirement</span></span> | <span data-ttu-id="31530-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="31530-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31530-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31530-137">Minimum supported client</span></span><br/> | <span data-ttu-id="31530-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31530-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="31530-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31530-139">Minimum supported server</span></span><br/> | <span data-ttu-id="31530-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31530-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="31530-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="31530-141">End of client support</span></span><br/>    | <span data-ttu-id="31530-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="31530-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="31530-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="31530-143">End of server support</span></span><br/>    | <span data-ttu-id="31530-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31530-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="31530-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31530-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31530-146">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="31530-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="31530-147">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="31530-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="31530-148">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="31530-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
