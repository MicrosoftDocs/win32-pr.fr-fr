---
description: Interface IEnumPStoreProviders-fournit des méthodes d’énumération COM pour l’interface IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: IEnumPStoreProviders, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089347"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="a3faf-103">Interface IEnumPStoreProviders</span><span class="sxs-lookup"><span data-stu-id="a3faf-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="a3faf-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a3faf-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a3faf-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a3faf-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a3faf-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="a3faf-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a3faf-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a3faf-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a3faf-108">Fournit des méthodes d’énumération COM standard pour l’interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="a3faf-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="a3faf-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a3faf-109">Members</span></span>

<span data-ttu-id="a3faf-110">L’interface **IEnumPStoreProviders** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a3faf-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a3faf-111">**IEnumPStoreProviders** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a3faf-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="a3faf-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3faf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a3faf-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3faf-113">Methods</span></span>

<span data-ttu-id="a3faf-114">L’interface **IEnumPStoreProviders** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3faf-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="a3faf-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="a3faf-115">Method</span></span>                                      | <span data-ttu-id="a3faf-116">Description</span><span class="sxs-lookup"><span data-stu-id="a3faf-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3faf-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="a3faf-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="a3faf-118">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="a3faf-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="a3faf-119">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="a3faf-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="a3faf-120">Obtient le fournisseur spécifié suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a3faf-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="a3faf-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="a3faf-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="a3faf-122">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a3faf-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="a3faf-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="a3faf-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="a3faf-124">Ignore le fournisseur spécifié dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a3faf-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="a3faf-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3faf-125">Requirements</span></span>



| <span data-ttu-id="a3faf-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3faf-126">Requirement</span></span> | <span data-ttu-id="a3faf-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3faf-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3faf-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3faf-128">Header</span></span><br/> | <dl> <span data-ttu-id="a3faf-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3faf-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a3faf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a3faf-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="a3faf-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3faf-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
