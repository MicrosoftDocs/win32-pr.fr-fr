---
description: 'IEnumMedia :: Clone, méthode-la méthode Clone crée un autre énumérateur qui contient le même état d’énumération que le même état d’énumération actuel.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'IEnumMedia :: Clone, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114547"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="a5484-103">IEnumMedia :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="a5484-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="a5484-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5484-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a5484-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a5484-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a5484-106">La méthode **clone** crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="a5484-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5484-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5484-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a5484-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5484-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5484-109">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5484-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5484-110">Pointeur vers le nouvel objet [**IEnumMedia**](ienummedia.md) .</span><span class="sxs-lookup"><span data-stu-id="a5484-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5484-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5484-111">Return value</span></span>

<span data-ttu-id="a5484-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a5484-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a5484-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5484-113">Value</span></span>                                                                                         | <span data-ttu-id="a5484-114">Signification</span><span class="sxs-lookup"><span data-stu-id="a5484-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a5484-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a5484-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5484-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a5484-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a5484-118">Le paramètre *ppEnum* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a5484-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="a5484-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a5484-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a5484-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a5484-121"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="a5484-122">A échoué pour des raisons inconnues.</span><span class="sxs-lookup"><span data-stu-id="a5484-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="a5484-123">Notes </span><span class="sxs-lookup"><span data-stu-id="a5484-123">Remarks</span></span>

<span data-ttu-id="a5484-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumMedia**](ienummedia.md) retournée par **IEnumMedia :: Clone**.</span><span class="sxs-lookup"><span data-stu-id="a5484-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="a5484-125">L’application doit appeler **Release** sur l’interface **IEnumMedia** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="a5484-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5484-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5484-126">Requirements</span></span>



| <span data-ttu-id="a5484-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5484-127">Requirement</span></span> | <span data-ttu-id="a5484-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5484-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5484-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a5484-129">TAPI version</span></span><br/> | <span data-ttu-id="a5484-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a5484-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a5484-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5484-131">Header</span></span><br/>       | <dl> <span data-ttu-id="a5484-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5484-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5484-133">Library</span></span><br/>      | <dl> <span data-ttu-id="a5484-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a5484-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a5484-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="a5484-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5484-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5484-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5484-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5484-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="a5484-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




