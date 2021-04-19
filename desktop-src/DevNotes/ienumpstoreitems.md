---
description: Fournit les méthodes d’énumération COM-standard pour l’interface IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: IEnumPStoreItems, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525409"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="516cc-103">Interface IEnumPStoreItems</span><span class="sxs-lookup"><span data-stu-id="516cc-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="516cc-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="516cc-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="516cc-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="516cc-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="516cc-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="516cc-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="516cc-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="516cc-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="516cc-108">Fournit les méthodes d’énumération COM-standard pour l’interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="516cc-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="516cc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="516cc-109">Members</span></span>

<span data-ttu-id="516cc-110">L’interface **IEnumPStoreItems** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="516cc-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="516cc-111">**IEnumPStoreItems** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="516cc-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="516cc-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="516cc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="516cc-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="516cc-113">Methods</span></span>

<span data-ttu-id="516cc-114">L’interface **IEnumPStoreItems** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="516cc-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="516cc-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="516cc-115">Method</span></span>                                  | <span data-ttu-id="516cc-116">Description</span><span class="sxs-lookup"><span data-stu-id="516cc-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="516cc-117">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="516cc-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="516cc-118">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="516cc-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="516cc-119">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="516cc-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="516cc-120">Obtient l’élément de données spécifié suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="516cc-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="516cc-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="516cc-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="516cc-122">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="516cc-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="516cc-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="516cc-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="516cc-124">Ignore l’élément de données spécifié dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="516cc-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="516cc-125">Notes</span><span class="sxs-lookup"><span data-stu-id="516cc-125">Remarks</span></span>

<span data-ttu-id="516cc-126">Il est nécessaire de libérer chaque élément après l’avoir énuméré.</span><span class="sxs-lookup"><span data-stu-id="516cc-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="516cc-127">L’objet énumérateur doit également être libéré lorsqu’il n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="516cc-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="516cc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="516cc-128">Requirements</span></span>



| <span data-ttu-id="516cc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="516cc-129">Requirement</span></span> | <span data-ttu-id="516cc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="516cc-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="516cc-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="516cc-131">Header</span></span><br/> | <dl> <span data-ttu-id="516cc-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="516cc-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="516cc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="516cc-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="516cc-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="516cc-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
