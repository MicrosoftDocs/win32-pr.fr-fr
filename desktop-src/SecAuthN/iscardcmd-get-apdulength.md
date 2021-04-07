---
description: Détermine la longueur, en octets, de l’unité de données du protocole d’application (APDU).
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'ISCardCmd :: get_ApduLength, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1535d2b4b67861b42719506ebd48cca4c49d5c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760114"
---
# <a name="iscardcmdget_apdulength-method"></a><span data-ttu-id="ed984-103">ISCardCmd :: \_ ApduLength, méthode</span><span class="sxs-lookup"><span data-stu-id="ed984-103">ISCardCmd::get\_ApduLength method</span></span>

<span data-ttu-id="ed984-104">\[La méthode **obtenir \_ ApduLength** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ed984-104">\[The **get\_ApduLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ed984-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ed984-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ed984-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ed984-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ed984-107">La méthode d' **extraction \_ ApduLength** détermine la longueur, en octets, de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="ed984-107">The **get\_ApduLength** method determines the length, in bytes, f the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed984-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed984-108">Syntax</span></span>


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="ed984-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed984-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed984-110">*plSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed984-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed984-111">Pointeur vers la longueur du APDU.</span><span class="sxs-lookup"><span data-stu-id="ed984-111">Pointer to the length of the APDU.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed984-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed984-112">Return value</span></span>

<span data-ttu-id="ed984-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed984-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ed984-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ed984-114">Return code</span></span>                                                                                   | <span data-ttu-id="ed984-115">Description</span><span class="sxs-lookup"><span data-stu-id="ed984-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ed984-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ed984-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ed984-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ed984-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ed984-119">Le paramètre *plSize* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ed984-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ed984-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ed984-121">Un pointeur incorrect a été passé dans *plSize*.</span><span class="sxs-lookup"><span data-stu-id="ed984-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="ed984-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ed984-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ed984-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ed984-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ed984-124">Remarks</span></span>

<span data-ttu-id="ed984-125">Pour récupérer l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU) brute à partir de la mémoire tampon d’octets mappée à l’aide d’un **IStream** qui contient le message APDU, appelez [**obtenir \_ APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="ed984-125">To retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="ed984-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ed984-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ed984-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="ed984-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ed984-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ed984-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ed984-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="ed984-129">Examples</span></span>

<span data-ttu-id="ed984-130">L’exemple suivant montre comment récupérer la longueur de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="ed984-130">The following example shows how to retrieve the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) length.</span></span> <span data-ttu-id="ed984-131">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="ed984-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="ed984-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed984-132">Requirements</span></span>



| <span data-ttu-id="ed984-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed984-133">Requirement</span></span> | <span data-ttu-id="ed984-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed984-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed984-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed984-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ed984-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed984-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ed984-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed984-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ed984-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed984-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed984-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ed984-139">End of client support</span></span><br/>    | <span data-ttu-id="ed984-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed984-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ed984-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ed984-141">End of server support</span></span><br/>    | <span data-ttu-id="ed984-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed984-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ed984-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed984-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed984-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed984-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ed984-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed984-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ed984-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ed984-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed984-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed984-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ed984-149">IID</span><span class="sxs-lookup"><span data-stu-id="ed984-149">IID</span></span><br/>                      | <span data-ttu-id="ed984-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ed984-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ed984-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed984-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed984-152">**Télécharger le \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="ed984-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="ed984-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ed984-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
