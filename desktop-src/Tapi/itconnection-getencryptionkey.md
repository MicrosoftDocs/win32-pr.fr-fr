---
description: La méthode GetEncryptionKey obtient la clé de chiffrement.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'ITConnection :: GetEncryptionKey, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537431"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="0a135-103">ITConnection :: GetEncryptionKey, méthode</span><span class="sxs-lookup"><span data-stu-id="0a135-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="0a135-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0a135-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0a135-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0a135-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0a135-106">La méthode **GetEncryptionKey** obtient la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0a135-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a135-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a135-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="0a135-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a135-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a135-109">*ppKeyType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a135-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a135-110">Pointeur vers un **BSTR** contenant le type de clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0a135-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="0a135-111">*pfValidKeyData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a135-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a135-112">Indique la validité des données de clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0a135-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="0a135-113">*ppKeyData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a135-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a135-114">Pointeur vers un **BSTR** contenant les données de clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0a135-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a135-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a135-115">Return value</span></span>

<span data-ttu-id="0a135-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0a135-116">This method can return one of these values.</span></span>



| <span data-ttu-id="0a135-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0a135-117">Return code</span></span>                                                                                   | <span data-ttu-id="0a135-118">Description</span><span class="sxs-lookup"><span data-stu-id="0a135-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a135-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0a135-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="0a135-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="0a135-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0a135-122">Le paramètre *ppKeyType, pfValidKeyData* ou *ppKeyData* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="0a135-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="0a135-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0a135-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0a135-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="0a135-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0a135-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0a135-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0a135-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0a135-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="0a135-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="0a135-129">Notes</span><span class="sxs-lookup"><span data-stu-id="0a135-129">Remarks</span></span>

<span data-ttu-id="0a135-130">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour les paramètres *ppKeyType* et *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="0a135-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a135-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a135-131">Requirements</span></span>



| <span data-ttu-id="0a135-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a135-132">Requirement</span></span> | <span data-ttu-id="0a135-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a135-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a135-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0a135-134">TAPI version</span></span><br/> | <span data-ttu-id="0a135-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0a135-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0a135-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a135-136">Header</span></span><br/>       | <dl> <span data-ttu-id="0a135-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a135-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a135-138">Library</span></span><br/>      | <dl> <span data-ttu-id="0a135-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0a135-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0a135-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="0a135-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a135-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a135-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a135-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a135-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="0a135-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

