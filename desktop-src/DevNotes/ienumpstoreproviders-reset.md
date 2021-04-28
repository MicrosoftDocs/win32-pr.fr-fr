---
description: 'IEnumPStoreProviders :: Reset, méthode-réinitialise au début de la séquence d’énumération.'
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: 'IEnumPStoreProviders :: Reset, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3e37e131b6f67f94bb787051123be8eb430eb39e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096757"
---
# <a name="ienumpstoreprovidersreset-method"></a><span data-ttu-id="34d49-103">IEnumPStoreProviders :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="34d49-103">IEnumPStoreProviders::Reset method</span></span>

<span data-ttu-id="34d49-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34d49-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="34d49-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="34d49-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="34d49-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="34d49-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="34d49-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="34d49-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="34d49-108">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="34d49-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d49-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34d49-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="34d49-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34d49-110">Parameters</span></span>

<span data-ttu-id="34d49-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="34d49-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34d49-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34d49-112">Return value</span></span>

<span data-ttu-id="34d49-113">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34d49-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d49-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34d49-114">Requirements</span></span>



| <span data-ttu-id="34d49-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34d49-115">Requirement</span></span> | <span data-ttu-id="34d49-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="34d49-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34d49-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="34d49-117">Header</span></span><br/> | <dl> <span data-ttu-id="34d49-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="34d49-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="34d49-119">DLL</span><span class="sxs-lookup"><span data-stu-id="34d49-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="34d49-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34d49-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d49-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34d49-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d49-122">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="34d49-122">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
