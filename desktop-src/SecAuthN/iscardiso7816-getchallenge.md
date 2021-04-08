---
description: La méthode GetChallenge construit une commande APDU (Application Protocol Data Unit) qui émet une stimulation (par exemple, un nombre aléatoire) à utiliser dans le cas d’une procédure liée à la sécurité.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: 'ISCardISO7816 :: GetChallenge, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034950"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="8911f-103">ISCardISO7816 :: GetChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="8911f-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="8911f-104">\[La méthode **GetChallenge** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8911f-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8911f-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8911f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8911f-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8911f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8911f-107">La méthode **GetChallenge** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui émet une stimulation (par exemple, un nombre aléatoire) à utiliser dans le cas d’une procédure liée à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="8911f-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8911f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8911f-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="8911f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8911f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8911f-110">*lBytesExpected* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8911f-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8911f-111">Longueur maximale de la réponse attendue.</span><span class="sxs-lookup"><span data-stu-id="8911f-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="8911f-112">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8911f-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8911f-113">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="8911f-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="8911f-114">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="8911f-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="8911f-115">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="8911f-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8911f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8911f-116">Return value</span></span>

<span data-ttu-id="8911f-117">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="8911f-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8911f-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8911f-118">Return code</span></span>                                                                                   | <span data-ttu-id="8911f-119">Description</span><span class="sxs-lookup"><span data-stu-id="8911f-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8911f-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8911f-121">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8911f-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8911f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8911f-123">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="8911f-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8911f-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8911f-125">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="8911f-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8911f-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8911f-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8911f-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8911f-128">Notes</span><span class="sxs-lookup"><span data-stu-id="8911f-128">Remarks</span></span>

<span data-ttu-id="8911f-129">La stimulation est valide au moins pour la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="8911f-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="8911f-130">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="8911f-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="8911f-131">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="8911f-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8911f-132">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8911f-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8911f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8911f-133">Requirements</span></span>



| <span data-ttu-id="8911f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8911f-134">Requirement</span></span> | <span data-ttu-id="8911f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8911f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8911f-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8911f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8911f-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8911f-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8911f-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8911f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8911f-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8911f-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8911f-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8911f-140">End of client support</span></span><br/>    | <span data-ttu-id="8911f-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8911f-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8911f-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8911f-142">End of server support</span></span><br/>    | <span data-ttu-id="8911f-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8911f-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8911f-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="8911f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8911f-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8911f-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8911f-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="8911f-147"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8911f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8911f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8911f-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8911f-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8911f-150">IID</span><span class="sxs-lookup"><span data-stu-id="8911f-150">IID</span></span><br/>                      | <span data-ttu-id="8911f-151">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8911f-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8911f-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8911f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8911f-153">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="8911f-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="8911f-154">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="8911f-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="8911f-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8911f-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
