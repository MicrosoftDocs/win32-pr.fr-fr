---
description: Obtient un objet énumérateur qui peut être utilisé à son tour pour énumérer les fournisseurs de stockage protégés qui sont actuellement installés sur le système.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Fonction PStoreEnumProviders (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540599"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="a6d0b-103">PStoreEnumProviders fonction)</span><span class="sxs-lookup"><span data-stu-id="a6d0b-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="a6d0b-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a6d0b-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a6d0b-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a6d0b-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a6d0b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a6d0b-108">Obtient un objet énumérateur qui peut être utilisé à son tour pour énumérer les fournisseurs de stockage protégés qui sont actuellement installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6d0b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6d0b-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="a6d0b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6d0b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6d0b-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a6d0b-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a6d0b-112">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a6d0b-113">*ppenum*</span><span class="sxs-lookup"><span data-stu-id="a6d0b-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="a6d0b-114">Pointeur vers un pointeur vers une interface [**IEnumPStoreProviders**](ienumpstoreproviders.md) qui peut être utilisée pour énumérer les fournisseurs installés.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6d0b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6d0b-115">Return value</span></span>

<span data-ttu-id="a6d0b-116">Cette fonction retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d0b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a6d0b-117">Remarks</span></span>

<span data-ttu-id="a6d0b-118">Le composant de stockage protégé a une architecture basée sur un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="a6d0b-119">Les applications qui utilisent le stockage protégé peuvent spécifier les fournisseurs installés à utiliser lors du stockage et de la récupération de leurs données.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="a6d0b-120">La fonction **PStoreEnumProviders** est utilisée pour énumérer les fournisseurs de stockage protégés installés.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="a6d0b-121">Chaque fournisseur est identifié par un identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="a6d0b-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="a6d0b-122">Jusqu’à présent, un seul fournisseur de stockage protégé a jamais été écrit.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="a6d0b-123">Étant donné que le service de stockage protégé est actuellement déconseillé, il est peu probable que des fournisseurs supplémentaires soient générés.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="a6d0b-124">Par conséquent, cette fonction ne doit pas être utilisée à quelque fin que ce soit.</span><span class="sxs-lookup"><span data-stu-id="a6d0b-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="a6d0b-125">Cette fonction n’a pas de bibliothèque d’importation associée ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a6d0b-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d0b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6d0b-126">Requirements</span></span>



| <span data-ttu-id="a6d0b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6d0b-127">Requirement</span></span> | <span data-ttu-id="a6d0b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6d0b-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d0b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6d0b-129">Header</span></span><br/> | <dl> <span data-ttu-id="a6d0b-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d0b-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a6d0b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a6d0b-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="a6d0b-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6d0b-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6d0b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6d0b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d0b-134">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="a6d0b-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
