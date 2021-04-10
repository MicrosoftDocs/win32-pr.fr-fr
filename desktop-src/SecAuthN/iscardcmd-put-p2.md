---
description: Définit le deuxième octet de paramètre (P2) dans l’unité de données de protocole d’application (APDU).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: ISCardCmd ::p ut_P2, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201245"
---
# <a name="iscardcmdput_p2-method"></a><span data-ttu-id="38542-103">ISCardCmd ::p ut \_ P2, méthode</span><span class="sxs-lookup"><span data-stu-id="38542-103">ISCardCmd::put\_P2 method</span></span>

<span data-ttu-id="38542-104">\[La méthode **put \_ P2** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="38542-104">\[The **put\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="38542-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="38542-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="38542-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="38542-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="38542-107">La méthode **put \_ P2** définit le deuxième octet de paramètre (P2) dans l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="38542-107">The **put\_P2** method sets the second parameter (P2) byte in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="38542-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38542-108">Syntax</span></span>


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a><span data-ttu-id="38542-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38542-110">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38542-110">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38542-111">Octet qui est le champ P2.</span><span class="sxs-lookup"><span data-stu-id="38542-111">The byte that is the P2 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38542-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38542-112">Return value</span></span>

<span data-ttu-id="38542-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="38542-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="38542-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="38542-114">Return code</span></span>                                                                                   | <span data-ttu-id="38542-115">Description</span><span class="sxs-lookup"><span data-stu-id="38542-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="38542-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38542-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="38542-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="38542-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="38542-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="38542-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="38542-119">Le paramètre *byP2* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="38542-119">The *byP2* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="38542-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="38542-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="38542-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="38542-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="38542-122">Notes</span><span class="sxs-lookup"><span data-stu-id="38542-122">Remarks</span></span>

<span data-ttu-id="38542-123">Pour définir la valeur P1 du APDU, appelez [**put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="38542-123">To set the P1 value of the APDU, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="38542-124">Pour récupérer les valeurs P1, P2 et P3 existantes, appelez [**obtenir \_ P1**](iscardcmd-get-p1.md), [**obtenir \_ P2**](iscardcmd-get-p2.md) ou [**obtenir \_ P3**](iscardcmd-get-p3.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="38542-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="38542-125">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="38542-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="38542-126">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="38542-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="38542-127">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="38542-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="38542-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="38542-128">Examples</span></span>

<span data-ttu-id="38542-129">L’exemple suivant montre comment définir le deuxième octet de paramètre (P2) de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="38542-129">The following example shows how to set the second parameter (P2) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="38542-130">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="38542-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="38542-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38542-131">Requirements</span></span>



| <span data-ttu-id="38542-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38542-132">Requirement</span></span> | <span data-ttu-id="38542-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="38542-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38542-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38542-134">Minimum supported client</span></span><br/> | <span data-ttu-id="38542-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38542-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="38542-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38542-136">Minimum supported server</span></span><br/> | <span data-ttu-id="38542-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38542-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38542-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="38542-138">End of client support</span></span><br/>    | <span data-ttu-id="38542-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="38542-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="38542-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="38542-140">End of server support</span></span><br/>    | <span data-ttu-id="38542-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38542-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="38542-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="38542-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="38542-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="38542-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="38542-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="38542-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="38542-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38542-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38542-146">DLL</span><span class="sxs-lookup"><span data-stu-id="38542-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38542-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38542-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="38542-148">IID</span><span class="sxs-lookup"><span data-stu-id="38542-148">IID</span></span><br/>                      | <span data-ttu-id="38542-149">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="38542-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="38542-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38542-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38542-151">**recevoir \_ P1**</span><span class="sxs-lookup"><span data-stu-id="38542-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="38542-152">**Télécharger \_ P2**</span><span class="sxs-lookup"><span data-stu-id="38542-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="38542-153">**Accédez à \_ P3**</span><span class="sxs-lookup"><span data-stu-id="38542-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="38542-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="38542-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="38542-155">**placer \_ P1**</span><span class="sxs-lookup"><span data-stu-id="38542-155">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
