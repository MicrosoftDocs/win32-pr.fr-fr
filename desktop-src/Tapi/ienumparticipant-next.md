---
description: La méthode suivante obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération. Cette méthode est masquée dans les Visual Basic et les langages de script.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'IEnumParticipant :: Next, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533471"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="76fd8-104">IEnumParticipant :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="76fd8-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="76fd8-105">\[**Ensuite** , il n’est pas possible de l’utiliser dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="76fd8-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="76fd8-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="76fd8-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="76fd8-107">La méthode **suivante** obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="76fd8-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="76fd8-108">Cette méthode est masquée dans les Visual Basic et les langages de script.</span><span class="sxs-lookup"><span data-stu-id="76fd8-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="76fd8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76fd8-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="76fd8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76fd8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76fd8-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76fd8-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fd8-112">Nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="76fd8-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="76fd8-113">*ppElements* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76fd8-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76fd8-114">Pointeur vers des interfaces [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .</span><span class="sxs-lookup"><span data-stu-id="76fd8-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="76fd8-115">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76fd8-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76fd8-116">Pointeur vers le nombre d’éléments réellement fournis.</span><span class="sxs-lookup"><span data-stu-id="76fd8-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="76fd8-117">Peut avoir la **valeur null** si *celt* est un.</span><span class="sxs-lookup"><span data-stu-id="76fd8-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76fd8-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76fd8-118">Return value</span></span>

<span data-ttu-id="76fd8-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="76fd8-119">This method can return one of these values.</span></span>



| <span data-ttu-id="76fd8-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="76fd8-120">Return code</span></span>                                                                                   | <span data-ttu-id="76fd8-121">Description</span><span class="sxs-lookup"><span data-stu-id="76fd8-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="76fd8-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="76fd8-123">La méthode a retourné la valeur *celt* Number of Elements.</span><span class="sxs-lookup"><span data-stu-id="76fd8-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="76fd8-124"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="76fd8-125">Le nombre d’éléments restants était inférieur à *celt*.</span><span class="sxs-lookup"><span data-stu-id="76fd8-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="76fd8-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="76fd8-127">Le paramètre *ppElements* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="76fd8-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="76fd8-128"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="76fd8-129">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="76fd8-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76fd8-130">Notes</span><span class="sxs-lookup"><span data-stu-id="76fd8-130">Remarks</span></span>

<span data-ttu-id="76fd8-131">L’interface TAPI appelle la méthode [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur l’interface [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) retournée par **IEnumParticipant :: Next**.</span><span class="sxs-lookup"><span data-stu-id="76fd8-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="76fd8-132">L’application doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur l’interface **ITAgentHandler** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="76fd8-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="76fd8-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76fd8-133">Requirements</span></span>



| <span data-ttu-id="76fd8-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76fd8-134">Requirement</span></span> | <span data-ttu-id="76fd8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="76fd8-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76fd8-136">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="76fd8-136">TAPI version</span></span><br/> | <span data-ttu-id="76fd8-137">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="76fd8-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="76fd8-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="76fd8-138">Header</span></span><br/>       | <dl> <span data-ttu-id="76fd8-139"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="76fd8-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="76fd8-140">Library</span></span><br/>      | <dl> <span data-ttu-id="76fd8-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="76fd8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="76fd8-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="76fd8-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76fd8-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="76fd8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76fd8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fd8-145">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="76fd8-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="76fd8-146">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="76fd8-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

