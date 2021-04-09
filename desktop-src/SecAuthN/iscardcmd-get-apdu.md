---
description: Récupère l’unité de données de protocole d’application (APDU) brute.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'ISCardCmd :: get_Apdu, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034002"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="7cd39-103">ISCardCmd :: obtient la \_ méthode APDU</span><span class="sxs-lookup"><span data-stu-id="7cd39-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="7cd39-104">\[La méthode **obtenir \_ APDU** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7cd39-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7cd39-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7cd39-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7cd39-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7cd39-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7cd39-107">La méthode **obtenir \_ APDU** récupère l’unité de [*données de protocole d’application*](../secgloss/a-gly.md) brute (APDU).</span><span class="sxs-lookup"><span data-stu-id="7cd39-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd39-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cd39-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="7cd39-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cd39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd39-110">*ppApdu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7cd39-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd39-111">Pointeur vers la mémoire tampon d’octets mappée via un objet **IStream** qui contient le message APDU au retour.</span><span class="sxs-lookup"><span data-stu-id="7cd39-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd39-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cd39-112">Return value</span></span>

<span data-ttu-id="7cd39-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="7cd39-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7cd39-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7cd39-114">Return code</span></span>                                                                                   | <span data-ttu-id="7cd39-115">Description</span><span class="sxs-lookup"><span data-stu-id="7cd39-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7cd39-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7cd39-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7cd39-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="7cd39-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7cd39-119">Le paramètre *ppApdu* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7cd39-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="7cd39-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7cd39-121">Un pointeur incorrect a été passé dans *ppApdu*.</span><span class="sxs-lookup"><span data-stu-id="7cd39-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="7cd39-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7cd39-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="7cd39-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="7cd39-124">Notes</span><span class="sxs-lookup"><span data-stu-id="7cd39-124">Remarks</span></span>

<span data-ttu-id="7cd39-125">Pour copier le APDU à partir d’un objet [**IByteBuffer**](ibytebuffer.md) (**IStream**) dans le APDU encapsulé dans cet objet d’interface, appelez [**put \_ APDU**](iscardcmd-put-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="7cd39-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="7cd39-126">Pour déterminer la longueur des APDU, appelez [**obtenir \_ ApduLength**](iscardcmd-get-apdulength.md).</span><span class="sxs-lookup"><span data-stu-id="7cd39-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="7cd39-127">Pour obtenir la liste de toutes les méthodes fournies par l’interface [**ISCardCmd**](iscardcmd.md) , consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7cd39-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="7cd39-128">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="7cd39-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7cd39-129">Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7cd39-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7cd39-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="7cd39-130">Examples</span></span>

<span data-ttu-id="7cd39-131">L’exemple suivant montre comment récupérer l’unité de [*données de protocole d’application*](../secgloss/a-gly.md) (APDU) brute.</span><span class="sxs-lookup"><span data-stu-id="7cd39-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7cd39-132">L’exemple suppose que pISCardCmd est un pointeur valide vers l’interface [**ISCardCmd**](iscardcmd.md) , et que pIByteApdu est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd39-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7cd39-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd39-133">Requirements</span></span>



| <span data-ttu-id="7cd39-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd39-134">Requirement</span></span> | <span data-ttu-id="7cd39-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd39-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd39-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd39-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd39-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd39-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7cd39-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd39-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd39-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd39-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cd39-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7cd39-140">End of client support</span></span><br/>    | <span data-ttu-id="7cd39-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7cd39-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7cd39-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7cd39-142">End of server support</span></span><br/>    | <span data-ttu-id="7cd39-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7cd39-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7cd39-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cd39-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd39-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cd39-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7cd39-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cd39-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cd39-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd39-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd39-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd39-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7cd39-150">IID</span><span class="sxs-lookup"><span data-stu-id="7cd39-150">IID</span></span><br/>                      | <span data-ttu-id="7cd39-151">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7cd39-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7cd39-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd39-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd39-153">**Obtient \_ ApduLength**</span><span class="sxs-lookup"><span data-stu-id="7cd39-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="7cd39-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="7cd39-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="7cd39-155">**placer \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="7cd39-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
