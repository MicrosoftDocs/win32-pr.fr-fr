---
description: La méthode encapsuler encapsule l’unité de données du protocole d’application de commande donnée dans une autre commande APDU pour la transmission vers une carte à puce.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'ISCardCmd :: encapsuler, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528268"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="e16d4-103">ISCardCmd :: encapsuler, méthode</span><span class="sxs-lookup"><span data-stu-id="e16d4-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="e16d4-104">\[La méthode **encapsuler** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e16d4-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e16d4-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e16d4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e16d4-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e16d4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e16d4-107">La méthode **encapsuler** encapsule l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) de commande donnée dans une autre commande APDU pour la transmission vers une carte à [*puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e16d4-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e16d4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e16d4-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="e16d4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e16d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16d4-110">*pApdu* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e16d4-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16d4-111">Pointeur vers le APDU à encapsuler.</span><span class="sxs-lookup"><span data-stu-id="e16d4-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="e16d4-112">*ApduType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e16d4-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16d4-113">Casse ISO 7816-4 pour les transmissions [*T = 0*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e16d4-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="e16d4-114">**\_Cas ISO \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e16d4-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="e16d4-115">**\_Cas ISO \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e16d4-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="e16d4-116">**\_Cas ISO \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e16d4-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="e16d4-117">**\_Cas ISO \_ 4**</span><span class="sxs-lookup"><span data-stu-id="e16d4-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e16d4-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e16d4-118">Return value</span></span>

<span data-ttu-id="e16d4-119">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="e16d4-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e16d4-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e16d4-120">Return code</span></span>                                                                                   | <span data-ttu-id="e16d4-121">Description</span><span class="sxs-lookup"><span data-stu-id="e16d4-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e16d4-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e16d4-123">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e16d4-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="e16d4-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e16d4-125">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="e16d4-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="e16d4-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e16d4-127">Un pointeur incorrect a été passé dans *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="e16d4-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="e16d4-128"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e16d4-129">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e16d4-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="e16d4-130">Notes</span><span class="sxs-lookup"><span data-stu-id="e16d4-130">Remarks</span></span>

<span data-ttu-id="e16d4-131">Pour générer une commande APDU, appelez [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="e16d4-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="e16d4-132">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="e16d4-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="e16d4-133">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="e16d4-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e16d4-134">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e16d4-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e16d4-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="e16d4-135">Examples</span></span>

<span data-ttu-id="e16d4-136">L’exemple suivant montre comment encapsuler une commande APDU.</span><span class="sxs-lookup"><span data-stu-id="e16d4-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="e16d4-137">L’exemple suppose que pIByteApdu est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e16d4-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e16d4-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e16d4-138">Requirements</span></span>



| <span data-ttu-id="e16d4-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e16d4-139">Requirement</span></span> | <span data-ttu-id="e16d4-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e16d4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e16d4-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e16d4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e16d4-142">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e16d4-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e16d4-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e16d4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e16d4-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e16d4-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e16d4-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e16d4-145">End of client support</span></span><br/>    | <span data-ttu-id="e16d4-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e16d4-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e16d4-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e16d4-147">End of server support</span></span><br/>    | <span data-ttu-id="e16d4-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e16d4-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e16d4-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="e16d4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e16d4-150"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e16d4-151">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e16d4-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="e16d4-152"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e16d4-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e16d4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e16d4-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e16d4-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e16d4-155">IID</span><span class="sxs-lookup"><span data-stu-id="e16d4-155">IID</span></span><br/>                      | <span data-ttu-id="e16d4-156">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e16d4-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e16d4-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e16d4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16d4-158">**BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="e16d4-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="e16d4-159">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e16d4-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
