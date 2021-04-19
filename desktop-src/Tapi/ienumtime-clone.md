---
description: La méthode Clone crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'IEnumTime :: Clone, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543913"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="53d3d-103">IEnumTime :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="53d3d-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="53d3d-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="53d3d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="53d3d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="53d3d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="53d3d-106">La méthode **clone** crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="53d3d-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d3d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53d3d-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="53d3d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53d3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d3d-109">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="53d3d-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53d3d-110">Pointeur vers le nouvel objet [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="53d3d-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d3d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53d3d-111">Return value</span></span>

<span data-ttu-id="53d3d-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="53d3d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="53d3d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="53d3d-113">Value</span></span>                                                                                         | <span data-ttu-id="53d3d-114">Signification</span><span class="sxs-lookup"><span data-stu-id="53d3d-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="53d3d-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="53d3d-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="53d3d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="53d3d-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="53d3d-118">Le paramètre *ppEnum* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="53d3d-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="53d3d-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="53d3d-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="53d3d-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="53d3d-121"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="53d3d-122">A échoué pour des raisons inconnues.</span><span class="sxs-lookup"><span data-stu-id="53d3d-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="53d3d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="53d3d-123">Remarks</span></span>

<span data-ttu-id="53d3d-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumTime**](ienumtime.md) retournée par **IEnumTime :: Clone**.</span><span class="sxs-lookup"><span data-stu-id="53d3d-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="53d3d-125">L’application doit appeler **Release** sur l’interface **IEnumTime** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="53d3d-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d3d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53d3d-126">Requirements</span></span>



| <span data-ttu-id="53d3d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53d3d-127">Requirement</span></span> | <span data-ttu-id="53d3d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="53d3d-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53d3d-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="53d3d-129">TAPI version</span></span><br/> | <span data-ttu-id="53d3d-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53d3d-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="53d3d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="53d3d-131">Header</span></span><br/>       | <dl> <span data-ttu-id="53d3d-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="53d3d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="53d3d-133">Library</span></span><br/>      | <dl> <span data-ttu-id="53d3d-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="53d3d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="53d3d-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="53d3d-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53d3d-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53d3d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53d3d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d3d-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="53d3d-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




