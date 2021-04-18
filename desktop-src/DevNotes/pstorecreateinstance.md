---
description: Récupère un pointeur d’interface vers un fournisseur de stockage.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Fonction PStoreCreateInstance (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526317"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="2046f-103">PStoreCreateInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="2046f-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="2046f-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2046f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2046f-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2046f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2046f-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="2046f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2046f-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="2046f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2046f-108">\[Cette fonction peut être modifiée ou non disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="2046f-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="2046f-109">Utilisez les fonctions **CryptProtectData** et **CryptUnprotectData** au lieu de cette fonction.\]</span><span class="sxs-lookup"><span data-stu-id="2046f-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="2046f-110">Récupère un pointeur d’interface vers un fournisseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="2046f-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="2046f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2046f-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2046f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2046f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2046f-113">*ppProvider* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2046f-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2046f-114">Pointeur vers le pointeur d’interface récupéré pour le fournisseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="2046f-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="2046f-115">Lorsque vous avez fini d’utiliser l’interface, décrémente son décompte de références en appelant sa méthode [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="2046f-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="2046f-116">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="2046f-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2046f-117">*pProviderID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2046f-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2046f-118">Pointeur vers le **GUID** qui identifie le fournisseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="2046f-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="2046f-119">Si ce paramètre a la **valeur null**, le fournisseur de stockage de base est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2046f-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="2046f-120">*conservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2046f-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2046f-121">Réservé doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2046f-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2046f-122">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2046f-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2046f-123">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2046f-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2046f-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2046f-124">Return value</span></span>

<span data-ttu-id="2046f-125">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2046f-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="2046f-126">La valeur **S \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="2046f-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2046f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2046f-127">Remarks</span></span>

<span data-ttu-id="2046f-128">Cette fonction n’a pas de bibliothèque d’importation associée ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2046f-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2046f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2046f-129">Requirements</span></span>



| <span data-ttu-id="2046f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2046f-130">Requirement</span></span> | <span data-ttu-id="2046f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2046f-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2046f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2046f-132">Header</span></span><br/> | <dl> <span data-ttu-id="2046f-133"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="2046f-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2046f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2046f-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="2046f-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2046f-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2046f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2046f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2046f-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="2046f-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="2046f-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="2046f-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
