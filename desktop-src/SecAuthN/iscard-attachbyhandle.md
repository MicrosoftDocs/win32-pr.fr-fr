---
description: Attache l’objet ISCard à un handle de carte à puce ouvert et configuré.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'ISCard :: AttachByHandle, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535544"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="24e34-103">ISCard :: AttachByHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="24e34-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="24e34-104">\[La méthode **AttachByHandle** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="24e34-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="24e34-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="24e34-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="24e34-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="24e34-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="24e34-107">La méthode **AttachByHandle** attache l’objet [**ISCard**](iscard.md) à un handle de [*carte à puce*](../secgloss/s-gly.md) ouvert et configuré.</span><span class="sxs-lookup"><span data-stu-id="24e34-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e34-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24e34-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="24e34-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24e34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e34-110">*hCard* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24e34-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24e34-111">Handle d’une connexion ouverte à une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="24e34-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e34-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24e34-112">Return value</span></span>

<span data-ttu-id="24e34-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="24e34-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="24e34-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="24e34-114">Return code</span></span>                                                                                  | <span data-ttu-id="24e34-115">Description</span><span class="sxs-lookup"><span data-stu-id="24e34-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="24e34-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24e34-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="24e34-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="24e34-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="24e34-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="24e34-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="24e34-119">Le paramètre *hCard* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="24e34-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24e34-120">Notes</span><span class="sxs-lookup"><span data-stu-id="24e34-120">Remarks</span></span>

<span data-ttu-id="24e34-121">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="24e34-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="24e34-122">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="24e34-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="24e34-123">Lorsque vous avez terminé d’utiliser le handle, libérez la pièce jointe en appelant la méthode [**ISCard ::D Etach**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="24e34-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="24e34-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="24e34-124">Examples</span></span>

<span data-ttu-id="24e34-125">L’exemple suivant illustre l’attachement à un handle de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="24e34-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="24e34-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24e34-126">Requirements</span></span>



| <span data-ttu-id="24e34-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24e34-127">Requirement</span></span> | <span data-ttu-id="24e34-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e34-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e34-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24e34-129">Minimum supported client</span></span><br/> | <span data-ttu-id="24e34-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24e34-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="24e34-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24e34-131">Minimum supported server</span></span><br/> | <span data-ttu-id="24e34-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24e34-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24e34-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="24e34-133">End of client support</span></span><br/>    | <span data-ttu-id="24e34-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="24e34-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="24e34-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="24e34-135">End of server support</span></span><br/>    | <span data-ttu-id="24e34-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="24e34-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="24e34-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="24e34-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="24e34-138"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e34-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="24e34-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="24e34-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="24e34-140"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24e34-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24e34-141">DLL</span><span class="sxs-lookup"><span data-stu-id="24e34-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24e34-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e34-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="24e34-143">IID</span><span class="sxs-lookup"><span data-stu-id="24e34-143">IID</span></span><br/>                      | <span data-ttu-id="24e34-144">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="24e34-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="24e34-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24e34-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e34-146">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="24e34-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="24e34-147">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="24e34-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="24e34-148">**Obtient \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="24e34-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="24e34-149">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="24e34-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="24e34-150">**Rattacher**</span><span class="sxs-lookup"><span data-stu-id="24e34-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
