---
description: La méthode SetEncryptionKey définit la clé de chiffrement nécessaire pour déchiffrer la session ou une indication à un mécanisme pour obtenir une clé utilisable par un moyen externe.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'ITConnection :: SetEncryptionKey, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539608"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="9e3fe-103">ITConnection :: SetEncryptionKey, méthode</span><span class="sxs-lookup"><span data-stu-id="9e3fe-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="9e3fe-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9e3fe-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="9e3fe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9e3fe-106">La méthode **SetEncryptionKey** définit la clé de chiffrement nécessaire pour déchiffrer la session ou une indication à un mécanisme pour obtenir une clé utilisable par un moyen externe.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e3fe-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="9e3fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e3fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3fe-109">*pKeyType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e3fe-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e3fe-110">Pointeur vers un **BSTR** contenant le type de clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="9e3fe-111">*ppKeyData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e3fe-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e3fe-112">Pointeur vers un **BSTR** contenant des informations sur la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3fe-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e3fe-113">Return value</span></span>

<span data-ttu-id="9e3fe-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9e3fe-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9e3fe-115">Return code</span></span>                                                                          | <span data-ttu-id="9e3fe-116">Description</span><span class="sxs-lookup"><span data-stu-id="9e3fe-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="9e3fe-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e3fe-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9e3fe-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e3fe-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9e3fe-119">Remarks</span></span>

<span data-ttu-id="9e3fe-120">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour les paramètres *pKeyType* et *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="9e3fe-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="9e3fe-121">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque les variables ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9e3fe-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3fe-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e3fe-122">Requirements</span></span>



| <span data-ttu-id="9e3fe-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e3fe-123">Requirement</span></span> | <span data-ttu-id="9e3fe-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e3fe-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3fe-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="9e3fe-125">TAPI version</span></span><br/> | <span data-ttu-id="9e3fe-126">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9e3fe-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9e3fe-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e3fe-127">Header</span></span><br/>       | <dl> <span data-ttu-id="9e3fe-128"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e3fe-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e3fe-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e3fe-129">Library</span></span><br/>      | <dl> <span data-ttu-id="9e3fe-130"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e3fe-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9e3fe-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9e3fe-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="9e3fe-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e3fe-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e3fe-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e3fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3fe-134">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="9e3fe-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

