---
description: La méthode Skip ignore le nombre spécifié d’éléments dans la séquence d’énumération. Cette méthode est masquée dans les Visual Basic et les langages de script.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'IEnumParticipant :: Skip, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526797"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="d8b12-104">IEnumParticipant :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="d8b12-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="d8b12-105">\[**Ignorer** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8b12-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d8b12-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d8b12-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d8b12-107">La méthode **Skip** ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="d8b12-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="d8b12-108">Cette méthode est masquée dans les Visual Basic et les langages de script.</span><span class="sxs-lookup"><span data-stu-id="d8b12-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b12-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b12-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="d8b12-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b12-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b12-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8b12-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b12-112">Nombre d'éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="d8b12-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b12-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8b12-113">Return value</span></span>

<span data-ttu-id="d8b12-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d8b12-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d8b12-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d8b12-115">Return code</span></span>                                                                                   | <span data-ttu-id="d8b12-116">Description</span><span class="sxs-lookup"><span data-stu-id="d8b12-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d8b12-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b12-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d8b12-118">Le nombre d’éléments ignorés était *celt*.</span><span class="sxs-lookup"><span data-stu-id="d8b12-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="d8b12-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b12-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="d8b12-120">Le nombre d’éléments ignorés n’est pas *celt*.</span><span class="sxs-lookup"><span data-stu-id="d8b12-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="d8b12-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b12-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d8b12-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d8b12-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8b12-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8b12-123">Requirements</span></span>



| <span data-ttu-id="d8b12-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8b12-124">Requirement</span></span> | <span data-ttu-id="d8b12-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8b12-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b12-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d8b12-126">TAPI version</span></span><br/> | <span data-ttu-id="d8b12-127">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d8b12-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d8b12-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8b12-128">Header</span></span><br/>       | <dl> <span data-ttu-id="d8b12-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b12-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="d8b12-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8b12-130">Library</span></span><br/>      | <dl> <span data-ttu-id="d8b12-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8b12-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d8b12-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b12-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="d8b12-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8b12-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d8b12-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b12-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b12-135">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="d8b12-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="d8b12-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="d8b12-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




