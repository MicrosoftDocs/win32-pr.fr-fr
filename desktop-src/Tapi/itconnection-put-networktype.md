---
description: La \_ méthode put NetworkType définit le type de réseau.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: ITConnection ::p ut_NetworkType, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535925"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="425c6-103">ITConnection ::p ut \_ NetworkType, méthode</span><span class="sxs-lookup"><span data-stu-id="425c6-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="425c6-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="425c6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="425c6-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="425c6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="425c6-106">La méthode **put \_ NetworkType** définit le type de réseau.</span><span class="sxs-lookup"><span data-stu-id="425c6-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="425c6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="425c6-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="425c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="425c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="425c6-109">*pNetworkType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="425c6-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="425c6-110">Pointeur vers un **BSTR** contenant le type de réseau.</span><span class="sxs-lookup"><span data-stu-id="425c6-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="425c6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="425c6-111">Return value</span></span>

<span data-ttu-id="425c6-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="425c6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="425c6-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="425c6-113">Return code</span></span>                                                                                   | <span data-ttu-id="425c6-114">Description</span><span class="sxs-lookup"><span data-stu-id="425c6-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="425c6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="425c6-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="425c6-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="425c6-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="425c6-118">Le paramètre *pNetworkType* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="425c6-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="425c6-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="425c6-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="425c6-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="425c6-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="425c6-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="425c6-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="425c6-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="425c6-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="425c6-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="425c6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="425c6-125">Remarks</span></span>

<span data-ttu-id="425c6-126">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PNetworkType* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="425c6-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="425c6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="425c6-127">Requirements</span></span>



| <span data-ttu-id="425c6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="425c6-128">Requirement</span></span> | <span data-ttu-id="425c6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="425c6-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="425c6-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="425c6-130">TAPI version</span></span><br/> | <span data-ttu-id="425c6-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="425c6-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="425c6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="425c6-132">Header</span></span><br/>       | <dl> <span data-ttu-id="425c6-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="425c6-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="425c6-134">Library</span></span><br/>      | <dl> <span data-ttu-id="425c6-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="425c6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="425c6-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="425c6-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="425c6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="425c6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425c6-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="425c6-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="425c6-140">**ITConnection :: obtient \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="425c6-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

