---
description: Copie l’unité de données du protocole d’application (APDU) à partir de l’objet IByteBuffer (IStream) dans le APDU encapsulé dans cet objet d’interface.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: ISCardCmd ::p ut_Apdu, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951195"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="74c50-103">ISCardCmd ::p ut ( \_ méthode APDU)</span><span class="sxs-lookup"><span data-stu-id="74c50-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="74c50-104">\[La méthode **put \_ APDU** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="74c50-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="74c50-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="74c50-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="74c50-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="74c50-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="74c50-107">La **méthode put \_ APDU** copie l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU) à partir de l’objet [**IBYTEBUFFER**](ibytebuffer.md) (**IStream**) dans le APDU encapsulé dans cet objet d’interface.</span><span class="sxs-lookup"><span data-stu-id="74c50-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c50-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74c50-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="74c50-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74c50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c50-110">*pApdu* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74c50-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c50-111">Pointeur vers la valeur APDU ISO 7816-4 à copier dans.</span><span class="sxs-lookup"><span data-stu-id="74c50-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c50-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74c50-112">Return value</span></span>

<span data-ttu-id="74c50-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="74c50-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="74c50-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="74c50-114">Return code</span></span>                                                                                   | <span data-ttu-id="74c50-115">Description</span><span class="sxs-lookup"><span data-stu-id="74c50-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="74c50-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="74c50-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="74c50-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="74c50-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="74c50-119">Le paramètre *pApdu* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="74c50-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="74c50-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="74c50-121">Un pointeur incorrect a été passé dans *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="74c50-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="74c50-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="74c50-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="74c50-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="74c50-124">Notes</span><span class="sxs-lookup"><span data-stu-id="74c50-124">Remarks</span></span>

<span data-ttu-id="74c50-125">Pour récupérer les APDU brutes à partir de la mémoire tampon d’octets mappée via un **IStream** qui contient le message APDU, appelez [**obtenir \_ APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="74c50-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="74c50-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="74c50-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="74c50-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="74c50-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="74c50-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="74c50-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="74c50-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="74c50-129">Examples</span></span>

<span data-ttu-id="74c50-130">L’exemple suivant montre comment copier un APDU à partir d’un objet [**IByteBuffer**](ibytebuffer.md) (**IStream**) dans le APDU encapsulé dans un objet d’interface.</span><span class="sxs-lookup"><span data-stu-id="74c50-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="74c50-131">L’exemple suppose que pIByteApdu est un pointeur valide vers une instance de **IByteBuffer** et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="74c50-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="74c50-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74c50-132">Requirements</span></span>



| <span data-ttu-id="74c50-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74c50-133">Requirement</span></span> | <span data-ttu-id="74c50-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="74c50-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74c50-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c50-135">Minimum supported client</span></span><br/> | <span data-ttu-id="74c50-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74c50-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74c50-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c50-137">Minimum supported server</span></span><br/> | <span data-ttu-id="74c50-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74c50-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74c50-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="74c50-139">End of client support</span></span><br/>    | <span data-ttu-id="74c50-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="74c50-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="74c50-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="74c50-141">End of server support</span></span><br/>    | <span data-ttu-id="74c50-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74c50-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="74c50-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="74c50-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="74c50-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="74c50-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="74c50-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="74c50-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74c50-147">DLL</span><span class="sxs-lookup"><span data-stu-id="74c50-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74c50-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74c50-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74c50-149">IID</span><span class="sxs-lookup"><span data-stu-id="74c50-149">IID</span></span><br/>                      | <span data-ttu-id="74c50-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="74c50-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="74c50-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74c50-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c50-152">**Télécharger le \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="74c50-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="74c50-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="74c50-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
