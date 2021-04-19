---
description: 'L’interface IEnumMedia fournit des méthodes d’énumération COM standard pour l’interface ITMedia. La méthode ITMediaCollection :: obtenir \_ EnumerationIf retourne un pointeur vers IEnumMedia.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interface IEnumMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525650"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="bd2a5-104">Interface IEnumMedia</span><span class="sxs-lookup"><span data-stu-id="bd2a5-104">IEnumMedia interface</span></span>

<span data-ttu-id="bd2a5-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bd2a5-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bd2a5-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bd2a5-107">L’interface **IEnumMedia** fournit des méthodes d’énumération COM standard pour l’interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2a5-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="bd2a5-108">La méthode [**ITMediaCollection :: obtenir \_ EnumerationIf**](itmediacollection-get-enumerationif.md) retourne un pointeur vers **IEnumMedia**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="bd2a5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="bd2a5-109">Members</span></span>

<span data-ttu-id="bd2a5-110">L’interface **IEnumMedia** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bd2a5-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd2a5-111">**IEnumMedia** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bd2a5-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="bd2a5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd2a5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd2a5-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd2a5-113">Methods</span></span>

<span data-ttu-id="bd2a5-114">L’interface **IEnumMedia** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="bd2a5-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="bd2a5-115">Method</span></span>                            | <span data-ttu-id="bd2a5-116">Description</span><span class="sxs-lookup"><span data-stu-id="bd2a5-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd2a5-117">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="bd2a5-118">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="bd2a5-119">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="bd2a5-120">Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="bd2a5-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="bd2a5-122">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="bd2a5-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="bd2a5-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="bd2a5-124">Ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="bd2a5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd2a5-125">Requirements</span></span>



| <span data-ttu-id="bd2a5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd2a5-126">Requirement</span></span> | <span data-ttu-id="bd2a5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd2a5-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2a5-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="bd2a5-128">TAPI version</span></span><br/> | <span data-ttu-id="bd2a5-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bd2a5-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bd2a5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd2a5-130">Header</span></span><br/>       | <dl> <span data-ttu-id="bd2a5-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2a5-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd2a5-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bd2a5-132">Library</span></span><br/>      | <dl> <span data-ttu-id="bd2a5-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd2a5-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bd2a5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bd2a5-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="bd2a5-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd2a5-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

