---
description: Récupère le troisième octet de paramètre (P3) à partir de l’unité de données de protocole d’application (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'ISCardCmd :: get_P3, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113223"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="9a815-103">ISCardCmd :: obtient \_ P3, méthode</span><span class="sxs-lookup"><span data-stu-id="9a815-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="9a815-104">\[La méthode **obtenir \_ P3** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9a815-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9a815-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9a815-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a815-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="9a815-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9a815-107">La méthode **obtenir \_ P3** récupère le troisième octet de paramètre (P3) à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="9a815-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9a815-108">Cette valeur d’octet en lecture seule représente la taille de la partie des données du APDU.</span><span class="sxs-lookup"><span data-stu-id="9a815-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a815-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a815-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="9a815-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a815-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a815-111">*pbyP3* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a815-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a815-112">Pointeur vers l’octet qui est le P3 de l’APDU au retour.</span><span class="sxs-lookup"><span data-stu-id="9a815-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a815-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a815-113">Return value</span></span>

<span data-ttu-id="9a815-114">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="9a815-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9a815-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9a815-115">Return code</span></span>                                                                                   | <span data-ttu-id="9a815-116">Description</span><span class="sxs-lookup"><span data-stu-id="9a815-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9a815-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9a815-118">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="9a815-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="9a815-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9a815-120">*PbyP3* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9a815-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="9a815-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9a815-122">Un pointeur incorrect a été passé dans *pbyP3*.</span><span class="sxs-lookup"><span data-stu-id="9a815-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="9a815-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9a815-124">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="9a815-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="9a815-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9a815-125">Remarks</span></span>

<span data-ttu-id="9a815-126">Le paramètre P3 est en lecture seule et ne peut donc pas être défini.</span><span class="sxs-lookup"><span data-stu-id="9a815-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="9a815-127">Pour accéder aux paramètres P1 ou P2, appelez la valeur [**\_ P1**](iscardcmd-get-p1.md) et [**accédez à \_ P2**](iscardcmd-get-p2.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="9a815-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="9a815-128">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9a815-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9a815-129">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="9a815-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9a815-130">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9a815-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9a815-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a815-131">Examples</span></span>

<span data-ttu-id="9a815-132">L’exemple suivant montre comment récupérer le troisième octet de paramètre (P3) à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="9a815-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9a815-133">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="9a815-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9a815-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a815-134">Requirements</span></span>



| <span data-ttu-id="9a815-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a815-135">Requirement</span></span> | <span data-ttu-id="9a815-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a815-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a815-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a815-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9a815-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a815-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9a815-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a815-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9a815-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a815-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a815-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9a815-141">End of client support</span></span><br/>    | <span data-ttu-id="9a815-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a815-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9a815-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9a815-143">End of server support</span></span><br/>    | <span data-ttu-id="9a815-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a815-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9a815-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a815-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a815-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a815-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9a815-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a815-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a815-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9a815-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a815-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a815-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a815-151">IID</span><span class="sxs-lookup"><span data-stu-id="9a815-151">IID</span></span><br/>                      | <span data-ttu-id="9a815-152">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9a815-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9a815-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a815-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a815-154">**recevoir \_ P1**</span><span class="sxs-lookup"><span data-stu-id="9a815-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="9a815-155">**Télécharger \_ P2**</span><span class="sxs-lookup"><span data-stu-id="9a815-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="9a815-156">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="9a815-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
