---
description: La méthode Clone crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel. Cette méthode est masquée dans les Visual Basic et les langages de script.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'IEnumParticipant :: Clone, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534894"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="8440b-104">IEnumParticipant :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="8440b-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="8440b-105">\[Le **clone** ne peut pas être utilisé dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8440b-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8440b-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8440b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8440b-107">La méthode **clone** crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="8440b-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="8440b-108">Cette méthode est masquée dans les Visual Basic et les langages de script.</span><span class="sxs-lookup"><span data-stu-id="8440b-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="8440b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8440b-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="8440b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8440b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8440b-111">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8440b-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8440b-112">Pointeur vers une nouvelle interface [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="8440b-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8440b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8440b-113">Return value</span></span>

<span data-ttu-id="8440b-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8440b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8440b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8440b-115">Return code</span></span>                                                                                   | <span data-ttu-id="8440b-116">Description</span><span class="sxs-lookup"><span data-stu-id="8440b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8440b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8440b-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8440b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8440b-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8440b-120">Le paramètre *ppEnum* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="8440b-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="8440b-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8440b-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8440b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8440b-123"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="8440b-124">A échoué pour des raisons inconnues.</span><span class="sxs-lookup"><span data-stu-id="8440b-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8440b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8440b-125">Remarks</span></span>

<span data-ttu-id="8440b-126">L’interface TAPI appelle la méthode [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur l’interface [**IEnumParticipant**](ienumparticipant.md) retournée par **IEnumParticipant :: Clone**.</span><span class="sxs-lookup"><span data-stu-id="8440b-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="8440b-127">L’application doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur l’interface **IEnumParticipant** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="8440b-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8440b-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8440b-128">Requirements</span></span>



| <span data-ttu-id="8440b-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8440b-129">Requirement</span></span> | <span data-ttu-id="8440b-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8440b-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8440b-131">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8440b-131">TAPI version</span></span><br/> | <span data-ttu-id="8440b-132">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8440b-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8440b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="8440b-133">Header</span></span><br/>       | <dl> <span data-ttu-id="8440b-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8440b-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8440b-135">Library</span></span><br/>      | <dl> <span data-ttu-id="8440b-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8440b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8440b-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="8440b-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8440b-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8440b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8440b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8440b-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="8440b-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="8440b-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="8440b-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

