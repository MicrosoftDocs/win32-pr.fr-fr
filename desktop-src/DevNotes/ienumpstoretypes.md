---
description: Interface IEnumPStoreTypes-fournit des méthodes d’énumération COM pour l’interface IPStore.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: IEnumPStoreTypes, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089357"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="a4192-103">Interface IEnumPStoreTypes</span><span class="sxs-lookup"><span data-stu-id="a4192-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="a4192-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4192-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a4192-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a4192-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a4192-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="a4192-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a4192-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a4192-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a4192-108">Fournit des méthodes d’énumération COM standard pour l’interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="a4192-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="a4192-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a4192-109">Members</span></span>

<span data-ttu-id="a4192-110">L’interface **IEnumPStoreTypes** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4192-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a4192-111">**IEnumPStoreTypes** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a4192-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="a4192-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a4192-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a4192-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a4192-113">Methods</span></span>

<span data-ttu-id="a4192-114">L’interface **IEnumPStoreTypes** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a4192-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="a4192-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="a4192-115">Method</span></span>                                  | <span data-ttu-id="a4192-116">Description</span><span class="sxs-lookup"><span data-stu-id="a4192-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4192-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="a4192-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="a4192-118">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="a4192-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="a4192-119">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="a4192-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="a4192-120">Obtient le type de fournisseur spécifié suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a4192-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="a4192-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="a4192-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="a4192-122">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a4192-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="a4192-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="a4192-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="a4192-124">Ignore le type de fournisseur spécifié dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a4192-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="a4192-125">Notes </span><span class="sxs-lookup"><span data-stu-id="a4192-125">Remarks</span></span>

<span data-ttu-id="a4192-126">L’objet énumérateur doit être libéré lorsqu’il n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="a4192-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4192-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4192-127">Requirements</span></span>



| <span data-ttu-id="a4192-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4192-128">Requirement</span></span> | <span data-ttu-id="a4192-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4192-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4192-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4192-130">Header</span></span><br/> | <dl> <span data-ttu-id="a4192-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4192-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a4192-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a4192-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="a4192-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4192-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
