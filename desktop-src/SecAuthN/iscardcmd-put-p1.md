---
description: Définit le premier octet de paramètre (P1) de l’unité de données de protocole d’application (APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: ISCardCmd ::p ut_P1, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540878"
---
# <a name="iscardcmdput_p1-method"></a><span data-ttu-id="e18f8-103">ISCardCmd ::p ut \_ P1, méthode</span><span class="sxs-lookup"><span data-stu-id="e18f8-103">ISCardCmd::put\_P1 method</span></span>

<span data-ttu-id="e18f8-104">\[La méthode **put \_ P1** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e18f8-104">\[The **put\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e18f8-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e18f8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e18f8-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e18f8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e18f8-107">La méthode **put \_ P1** définit le premier octet de paramètre (P1) de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="e18f8-107">The **put\_P1** method sets the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="e18f8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e18f8-108">Syntax</span></span>


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a><span data-ttu-id="e18f8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e18f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e18f8-110">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e18f8-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e18f8-111">Octet qui est le champ P1.</span><span class="sxs-lookup"><span data-stu-id="e18f8-111">The byte that is the P1 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e18f8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e18f8-112">Return value</span></span>

<span data-ttu-id="e18f8-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="e18f8-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e18f8-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e18f8-114">Return code</span></span>                                                                                   | <span data-ttu-id="e18f8-115">Description</span><span class="sxs-lookup"><span data-stu-id="e18f8-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e18f8-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e18f8-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e18f8-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e18f8-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="e18f8-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e18f8-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e18f8-119">Le paramètre *byP1* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e18f8-119">The *byP1* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e18f8-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e18f8-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e18f8-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e18f8-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e18f8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e18f8-122">Remarks</span></span>

<span data-ttu-id="e18f8-123">Pour définir la valeur P2 du APDU, appelez la [**valeur \_ P2**](iscardcmd-get-p2.md).</span><span class="sxs-lookup"><span data-stu-id="e18f8-123">To set the P2 value of the APDU, call [**get\_P2**](iscardcmd-get-p2.md).</span></span>

<span data-ttu-id="e18f8-124">Pour récupérer les valeurs P1, P2 et P3 existantes, appelez [**obtenir \_ P1**](iscardcmd-get-p1.md), [**obtenir \_ P2**](iscardcmd-get-p2.md) ou [**obtenir \_ P3**](iscardcmd-get-p3.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="e18f8-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="e18f8-125">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="e18f8-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="e18f8-126">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="e18f8-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e18f8-127">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e18f8-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e18f8-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="e18f8-128">Examples</span></span>

<span data-ttu-id="e18f8-129">L’exemple suivant montre comment définir le premier octet de paramètre (P1) de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="e18f8-129">The following example shows how to set the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="e18f8-130">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="e18f8-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e18f8-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e18f8-131">Requirements</span></span>



| <span data-ttu-id="e18f8-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e18f8-132">Requirement</span></span> | <span data-ttu-id="e18f8-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e18f8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e18f8-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e18f8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e18f8-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e18f8-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e18f8-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e18f8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e18f8-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e18f8-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e18f8-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e18f8-138">End of client support</span></span><br/>    | <span data-ttu-id="e18f8-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e18f8-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e18f8-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e18f8-140">End of server support</span></span><br/>    | <span data-ttu-id="e18f8-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e18f8-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e18f8-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="e18f8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e18f8-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e18f8-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e18f8-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e18f8-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="e18f8-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e18f8-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e18f8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e18f8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e18f8-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e18f8-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e18f8-148">IID</span><span class="sxs-lookup"><span data-stu-id="e18f8-148">IID</span></span><br/>                      | <span data-ttu-id="e18f8-149">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e18f8-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e18f8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e18f8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18f8-151">**recevoir \_ P1**</span><span class="sxs-lookup"><span data-stu-id="e18f8-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="e18f8-152">**Télécharger \_ P2**</span><span class="sxs-lookup"><span data-stu-id="e18f8-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="e18f8-153">**Accédez à \_ P3**</span><span class="sxs-lookup"><span data-stu-id="e18f8-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="e18f8-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e18f8-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="e18f8-155">**put \_ P2**</span><span class="sxs-lookup"><span data-stu-id="e18f8-155">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
