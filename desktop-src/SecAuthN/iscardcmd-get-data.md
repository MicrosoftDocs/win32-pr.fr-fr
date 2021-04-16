---
description: Récupère le champ de données à partir de l’unité de données du protocole d’application (APDU), en le plaçant dans un objet de mémoire tampon d’octets.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'ISCardCmd :: get_Data, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530220"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="1bc96-103">ISCardCmd :: méthode d’extraction de \_ données</span><span class="sxs-lookup"><span data-stu-id="1bc96-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="1bc96-104">\[La méthode **obtenir des \_ données** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1bc96-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1bc96-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1bc96-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1bc96-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1bc96-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1bc96-107">La méthode **obtenir des \_ données** récupère le champ de données à partir de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU), en le plaçant dans un objet de mémoire tampon d’octets.</span><span class="sxs-lookup"><span data-stu-id="1bc96-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc96-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bc96-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="1bc96-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bc96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc96-110">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bc96-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc96-111">Pointeur vers l’objet de mémoire tampon d’octets (**IStream**) qui contient le champ de données APDU au retour.</span><span class="sxs-lookup"><span data-stu-id="1bc96-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc96-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bc96-112">Return value</span></span>

<span data-ttu-id="1bc96-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="1bc96-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1bc96-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1bc96-114">Return code</span></span>                                                                                   | <span data-ttu-id="1bc96-115">Description</span><span class="sxs-lookup"><span data-stu-id="1bc96-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1bc96-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1bc96-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1bc96-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="1bc96-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1bc96-119">Le paramètre *ppData* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1bc96-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="1bc96-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1bc96-121">Un pointeur incorrect a été passé dans *ppData*.</span><span class="sxs-lookup"><span data-stu-id="1bc96-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="1bc96-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1bc96-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1bc96-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="1bc96-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1bc96-124">Remarks</span></span>

<span data-ttu-id="1bc96-125">Pour définir le champ de données du APDU, appelez [**put \_ Data**](iscardcmd-put-data.md).</span><span class="sxs-lookup"><span data-stu-id="1bc96-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="1bc96-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="1bc96-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="1bc96-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="1bc96-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1bc96-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1bc96-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1bc96-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="1bc96-129">Examples</span></span>

<span data-ttu-id="1bc96-130">L’exemple suivant montre comment récupérer le champ de données de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="1bc96-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="1bc96-131">L’exemple suppose que pIByteData est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) , et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc96-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="1bc96-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bc96-132">Requirements</span></span>



| <span data-ttu-id="1bc96-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bc96-133">Requirement</span></span> | <span data-ttu-id="1bc96-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc96-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc96-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc96-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc96-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc96-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1bc96-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc96-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc96-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc96-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1bc96-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1bc96-139">End of client support</span></span><br/>    | <span data-ttu-id="1bc96-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1bc96-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1bc96-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1bc96-141">End of server support</span></span><br/>    | <span data-ttu-id="1bc96-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1bc96-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1bc96-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bc96-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bc96-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1bc96-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1bc96-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="1bc96-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1bc96-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc96-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bc96-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc96-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1bc96-149">IID</span><span class="sxs-lookup"><span data-stu-id="1bc96-149">IID</span></span><br/>                      | <span data-ttu-id="1bc96-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1bc96-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1bc96-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bc96-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc96-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="1bc96-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="1bc96-153">**placer des \_ données**</span><span class="sxs-lookup"><span data-stu-id="1bc96-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
