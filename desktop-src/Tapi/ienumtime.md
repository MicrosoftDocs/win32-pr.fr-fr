---
description: 'L’interface IEnumTime fournit des méthodes d’énumération COM standard pour l’interface ITTime. La méthode ITTimeCollection :: obtenir \_ EnumerationIf retourne un pointeur vers IEnumTime.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interface IEnumTime (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539226"
---
# <a name="ienumtime-interface"></a><span data-ttu-id="7e8a4-104">Interface IEnumTime</span><span class="sxs-lookup"><span data-stu-id="7e8a4-104">IEnumTime interface</span></span>

<span data-ttu-id="7e8a4-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e8a4-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7e8a4-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7e8a4-107">L’interface **IEnumTime** fournit des méthodes d’énumération COM standard pour l’interface [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="7e8a4-107">The **IEnumTime** interface provides COM-standard enumeration methods for the [**ITTime**](ittime.md) interface.</span></span> <span data-ttu-id="7e8a4-108">La méthode [**ITTimeCollection :: obtenir \_ EnumerationIf**](ittimecollection-get-enumerationif.md) retourne un pointeur vers **IEnumTime**.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-108">The [**ITTimeCollection::get\_EnumerationIf**](ittimecollection-get-enumerationif.md) method returns a pointer to **IEnumTime**.</span></span>

## <a name="members"></a><span data-ttu-id="7e8a4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7e8a4-109">Members</span></span>

<span data-ttu-id="7e8a4-110">L’interface **IEnumTime** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7e8a4-110">The **IEnumTime** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7e8a4-111">**IEnumTime** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e8a4-111">**IEnumTime** also has these types of members:</span></span>

-   [<span data-ttu-id="7e8a4-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7e8a4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7e8a4-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7e8a4-113">Methods</span></span>

<span data-ttu-id="7e8a4-114">L’interface **IEnumTime** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-114">The **IEnumTime** interface has these methods.</span></span>



| <span data-ttu-id="7e8a4-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7e8a4-115">Method</span></span>                           | <span data-ttu-id="7e8a4-116">Description</span><span class="sxs-lookup"><span data-stu-id="7e8a4-116">Description</span></span>                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e8a4-117">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="7e8a4-117">**Clone**</span></span>](ienumtime-clone.md) | <span data-ttu-id="7e8a4-118">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="7e8a4-119">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="7e8a4-119">**Next**</span></span>](ienumtime-next.md)   | <span data-ttu-id="7e8a4-120">Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="7e8a4-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="7e8a4-121">**Reset**</span></span>](ienumtime-reset.md) | <span data-ttu-id="7e8a4-122">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="7e8a4-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="7e8a4-123">**Skip**</span></span>](ienumtime-skip.md)   | <span data-ttu-id="7e8a4-124">Ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="7e8a4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e8a4-125">Requirements</span></span>



| <span data-ttu-id="7e8a4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e8a4-126">Requirement</span></span> | <span data-ttu-id="7e8a4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e8a4-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8a4-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7e8a4-128">TAPI version</span></span><br/> | <span data-ttu-id="7e8a4-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7e8a4-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7e8a4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e8a4-130">Header</span></span><br/>       | <dl> <span data-ttu-id="7e8a4-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e8a4-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e8a4-132">Library</span></span><br/>      | <dl> <span data-ttu-id="7e8a4-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7e8a4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7e8a4-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="7e8a4-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

