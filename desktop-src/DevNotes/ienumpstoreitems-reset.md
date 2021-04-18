---
description: Réinitialise au début de la séquence d’énumération donnée.
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: 'IEnumPStoreItems :: Reset, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d5b05c23ba40ab647b2c4b3bb552f92ee34e12c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526420"
---
# <a name="ienumpstoreitemsreset-method"></a><span data-ttu-id="c664a-103">IEnumPStoreItems :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="c664a-103">IEnumPStoreItems::Reset method</span></span>

<span data-ttu-id="c664a-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c664a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c664a-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c664a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c664a-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="c664a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c664a-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="c664a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c664a-108">Réinitialise au début de la séquence d’énumération donnée.</span><span class="sxs-lookup"><span data-stu-id="c664a-108">Resets to the beginning of the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c664a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c664a-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="c664a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c664a-110">Parameters</span></span>

<span data-ttu-id="c664a-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c664a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c664a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c664a-112">Return value</span></span>

<span data-ttu-id="c664a-113">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c664a-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c664a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c664a-114">Requirements</span></span>



| <span data-ttu-id="c664a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c664a-115">Requirement</span></span> | <span data-ttu-id="c664a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c664a-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c664a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c664a-117">Header</span></span><br/> | <dl> <span data-ttu-id="c664a-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="c664a-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c664a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c664a-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="c664a-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c664a-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c664a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c664a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c664a-122">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="c664a-122">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
