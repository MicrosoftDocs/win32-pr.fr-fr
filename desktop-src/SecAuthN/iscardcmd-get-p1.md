---
description: Récupère le premier paramètre (P1) octet de l’unité de données de protocole d’application (APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'ISCardCmd :: get_P1, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 047732fd8602828cc0501d623c57653bfdc9044f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526355"
---
# <a name="iscardcmdget_p1-method"></a><span data-ttu-id="175ea-103">ISCardCmd :: obtient la \_ méthode P1</span><span class="sxs-lookup"><span data-stu-id="175ea-103">ISCardCmd::get\_P1 method</span></span>

<span data-ttu-id="175ea-104">\[La méthode **obtenir \_ P1** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="175ea-104">\[The **get\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="175ea-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="175ea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="175ea-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="175ea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="175ea-107">La méthode **obtenir \_ P1** récupère le premier paramètre (P1) octet de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="175ea-107">The **get\_P1** method retrieves the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="175ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="175ea-108">Syntax</span></span>


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a><span data-ttu-id="175ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="175ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175ea-110">*pbyP1* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="175ea-110">*pbyP1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="175ea-111">Pointeur vers l’octet P1 dans le APDU au retour.</span><span class="sxs-lookup"><span data-stu-id="175ea-111">Pointer to the P1 byte in the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="175ea-112">Return value</span></span>

<span data-ttu-id="175ea-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="175ea-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="175ea-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="175ea-114">Return code</span></span>                                                                                   | <span data-ttu-id="175ea-115">Description</span><span class="sxs-lookup"><span data-stu-id="175ea-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="175ea-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="175ea-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="175ea-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="175ea-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="175ea-119">Le paramètre *pbyP1* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="175ea-119">The *pbyP1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="175ea-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="175ea-121">Un pointeur incorrect a été passé dans *pbyP1*.</span><span class="sxs-lookup"><span data-stu-id="175ea-121">A bad pointer was passed in *pbyP1*.</span></span><br/> |
| <dl> <span data-ttu-id="175ea-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="175ea-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="175ea-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="175ea-124">Notes</span><span class="sxs-lookup"><span data-stu-id="175ea-124">Remarks</span></span>

<span data-ttu-id="175ea-125">Pour définir le paramètre P1 sur une nouvelle valeur, appelez [**put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="175ea-125">To set the P1 parameter to a new value, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="175ea-126">Pour accéder aux paramètres P2 ou P3, appelez la vue d' [**avoir \_ P2**](iscardcmd-get-p2.md) et [**accédez à \_ P3**](iscardcmd-get-p3.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="175ea-126">To get the P2 or P3 parameters, call [**get\_P2**](iscardcmd-get-p2.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="175ea-127">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="175ea-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="175ea-128">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="175ea-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="175ea-129">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="175ea-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="175ea-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="175ea-130">Examples</span></span>

<span data-ttu-id="175ea-131">L’exemple suivant montre comment récupérer le premier octet de paramètre (P1) à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="175ea-131">The following example shows how to retrieve the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="175ea-132">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="175ea-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="175ea-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="175ea-133">Requirements</span></span>



| <span data-ttu-id="175ea-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="175ea-134">Requirement</span></span> | <span data-ttu-id="175ea-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="175ea-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="175ea-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="175ea-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="175ea-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="175ea-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="175ea-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="175ea-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="175ea-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="175ea-140">End of client support</span></span><br/>    | <span data-ttu-id="175ea-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="175ea-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="175ea-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="175ea-142">End of server support</span></span><br/>    | <span data-ttu-id="175ea-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="175ea-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="175ea-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="175ea-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="175ea-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="175ea-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="175ea-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="175ea-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="175ea-148">DLL</span><span class="sxs-lookup"><span data-stu-id="175ea-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="175ea-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="175ea-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="175ea-150">IID</span><span class="sxs-lookup"><span data-stu-id="175ea-150">IID</span></span><br/>                      | <span data-ttu-id="175ea-151">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="175ea-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="175ea-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="175ea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175ea-153">**Télécharger \_ P2**</span><span class="sxs-lookup"><span data-stu-id="175ea-153">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="175ea-154">**Accédez à \_ P3**</span><span class="sxs-lookup"><span data-stu-id="175ea-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="175ea-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="175ea-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="175ea-156">**placer \_ P1**</span><span class="sxs-lookup"><span data-stu-id="175ea-156">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
