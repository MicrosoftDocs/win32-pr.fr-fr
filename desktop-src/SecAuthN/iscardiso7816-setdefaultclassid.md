---
description: La méthode SetDefaultClassId affecte un octet d’identificateur de classe standard qui sera utilisé dans toutes les opérations lors de la construction d’une unité de données de protocole d’application (APDU) de commande ISO 7816-4. Par défaut, l’octet de l’identificateur de classe standard est 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'ISCardISO7816 :: SetDefaultClassId, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530582"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="2c0ea-104">ISCardISO7816 :: SetDefaultClassId, méthode</span><span class="sxs-lookup"><span data-stu-id="2c0ea-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="2c0ea-105">\[La méthode **SetDefaultClassId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c0ea-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c0ea-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2c0ea-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2c0ea-108">La méthode **SetDefaultClassId** affecte un octet d’identificateur de classe standard qui sera utilisé dans toutes les opérations lors de la construction d’une [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU) de commande ISO 7816-4.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="2c0ea-109">Par défaut, l’octet de l’identificateur de classe standard est 0x00.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0ea-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c0ea-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="2c0ea-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c0ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c0ea-112">*byClass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c0ea-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c0ea-113">Octet de l’ID de classe.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c0ea-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c0ea-114">Return value</span></span>

<span data-ttu-id="2c0ea-115">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c0ea-115">The possible return values are the following:</span></span>



| <span data-ttu-id="2c0ea-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2c0ea-116">Return code</span></span>                                                                          | <span data-ttu-id="2c0ea-117">Description</span><span class="sxs-lookup"><span data-stu-id="2c0ea-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2c0ea-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0ea-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2c0ea-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="2c0ea-120">Pour obtenir la liste de toutes les méthodes fournies par l’interface [**ISCardISO7816**](iscardiso7816.md) , consultez **ISCardISO7816**.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="2c0ea-121">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="2c0ea-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2c0ea-122">Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2c0ea-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0ea-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c0ea-123">Requirements</span></span>



| <span data-ttu-id="2c0ea-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c0ea-124">Requirement</span></span> | <span data-ttu-id="2c0ea-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c0ea-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0ea-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c0ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2c0ea-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c0ea-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c0ea-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c0ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2c0ea-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c0ea-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c0ea-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2c0ea-130">End of client support</span></span><br/>    | <span data-ttu-id="2c0ea-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c0ea-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2c0ea-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2c0ea-132">End of server support</span></span><br/>    | <span data-ttu-id="2c0ea-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c0ea-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2c0ea-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c0ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c0ea-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c0ea-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c0ea-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2c0ea-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c0ea-137"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c0ea-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c0ea-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c0ea-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c0ea-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c0ea-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c0ea-140">IID</span><span class="sxs-lookup"><span data-stu-id="2c0ea-140">IID</span></span><br/>                      | <span data-ttu-id="2c0ea-141">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2c0ea-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2c0ea-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c0ea-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0ea-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="2c0ea-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
