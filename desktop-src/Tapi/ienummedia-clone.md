---
description: La méthode Clone crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'IEnumMedia :: Clone, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29671819db202643506cbdf90a1550abb305718
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544367"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="a0f47-103">IEnumMedia :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="a0f47-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="a0f47-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a0f47-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0f47-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a0f47-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a0f47-106">La méthode **clone** crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="a0f47-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0f47-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a0f47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0f47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f47-109">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a0f47-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f47-110">Pointeur vers le nouvel objet [**IEnumMedia**](ienummedia.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f47-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f47-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0f47-111">Return value</span></span>

<span data-ttu-id="a0f47-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a0f47-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a0f47-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0f47-113">Value</span></span>                                                                                         | <span data-ttu-id="a0f47-114">Signification</span><span class="sxs-lookup"><span data-stu-id="a0f47-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a0f47-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a0f47-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a0f47-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a0f47-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a0f47-118">Le paramètre *ppEnum* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a0f47-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="a0f47-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a0f47-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a0f47-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a0f47-121"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="a0f47-122">A échoué pour des raisons inconnues.</span><span class="sxs-lookup"><span data-stu-id="a0f47-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="a0f47-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a0f47-123">Remarks</span></span>

<span data-ttu-id="a0f47-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumMedia**](ienummedia.md) retournée par **IEnumMedia :: Clone**.</span><span class="sxs-lookup"><span data-stu-id="a0f47-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="a0f47-125">L’application doit appeler **Release** sur l’interface **IEnumMedia** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="a0f47-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f47-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0f47-126">Requirements</span></span>



| <span data-ttu-id="a0f47-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0f47-127">Requirement</span></span> | <span data-ttu-id="a0f47-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0f47-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f47-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a0f47-129">TAPI version</span></span><br/> | <span data-ttu-id="a0f47-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a0f47-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a0f47-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0f47-131">Header</span></span><br/>       | <dl> <span data-ttu-id="a0f47-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0f47-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0f47-133">Library</span></span><br/>      | <dl> <span data-ttu-id="a0f47-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a0f47-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a0f47-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="a0f47-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0f47-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f47-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0f47-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f47-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="a0f47-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




