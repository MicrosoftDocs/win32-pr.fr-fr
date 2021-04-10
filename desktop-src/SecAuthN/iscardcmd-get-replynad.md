---
description: Récupère l’adresse de nœud (NAD) utilisée par la carte à puce dans le message de réponse.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'ISCardCmd :: get_ReplyNad, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113219"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="31e2e-103">ISCardCmd :: \_ ReplyNad, méthode</span><span class="sxs-lookup"><span data-stu-id="31e2e-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="31e2e-104">\[La méthode **obtenir \_ ReplyNad** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="31e2e-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31e2e-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="31e2e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="31e2e-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="31e2e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="31e2e-107">La méthode **obtenir \_ ReplyNad** récupère l’adresse de nœud (NAD) utilisée par la [*carte à puce*](../secgloss/s-gly.md) dans le message de réponse.</span><span class="sxs-lookup"><span data-stu-id="31e2e-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e2e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31e2e-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="31e2e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31e2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e2e-110">*pbNad* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="31e2e-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31e2e-111">Pointeur vers l’octet qui contient le NAD utilisé par le message de réponse, au retour.</span><span class="sxs-lookup"><span data-stu-id="31e2e-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e2e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31e2e-112">Return value</span></span>

<span data-ttu-id="31e2e-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="31e2e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="31e2e-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="31e2e-114">Return code</span></span>                                                                                    | <span data-ttu-id="31e2e-115">Description</span><span class="sxs-lookup"><span data-stu-id="31e2e-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="31e2e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31e2e-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="31e2e-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="31e2e-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="31e2e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="31e2e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="31e2e-119">Le paramètre *pbNad* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="31e2e-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="31e2e-120"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="31e2e-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="31e2e-121">Les appels internes n’ont pas pu récupérer les informations du NAD.</span><span class="sxs-lookup"><span data-stu-id="31e2e-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31e2e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="31e2e-122">Remarks</span></span>

<span data-ttu-id="31e2e-123">Outre les codes d’erreur COM listés ci-dessus, cette méthode peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="31e2e-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="31e2e-124">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="31e2e-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31e2e-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="31e2e-125">Examples</span></span>

<span data-ttu-id="31e2e-126">L’exemple suivant montre comment récupérer l’adresse de nœud (NAD) utilisée par la [*carte à puce*](../secgloss/s-gly.md) dans le message de réponse.</span><span class="sxs-lookup"><span data-stu-id="31e2e-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="31e2e-127">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="31e2e-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="31e2e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31e2e-128">Requirements</span></span>



| <span data-ttu-id="31e2e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31e2e-129">Requirement</span></span> | <span data-ttu-id="31e2e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="31e2e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31e2e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e2e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="31e2e-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31e2e-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31e2e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e2e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="31e2e-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31e2e-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31e2e-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="31e2e-135">End of client support</span></span><br/>    | <span data-ttu-id="31e2e-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="31e2e-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="31e2e-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="31e2e-137">End of server support</span></span><br/>    | <span data-ttu-id="31e2e-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31e2e-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="31e2e-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="31e2e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e2e-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="31e2e-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="31e2e-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="31e2e-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="31e2e-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31e2e-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="31e2e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="31e2e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31e2e-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31e2e-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="31e2e-145">IID</span><span class="sxs-lookup"><span data-stu-id="31e2e-145">IID</span></span><br/>                      | <span data-ttu-id="31e2e-146">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="31e2e-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="31e2e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31e2e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e2e-148">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="31e2e-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
