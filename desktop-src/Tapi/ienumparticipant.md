---
description: 'L’interface IEnumParticipant fournit des méthodes d’énumération COM standard pour l’interface ITParticipant. La méthode ITParticipantControl :: EnumerateParticipants retourne un pointeur vers IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interface IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533394"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="29ed4-104">Interface IEnumParticipant</span><span class="sxs-lookup"><span data-stu-id="29ed4-104">IEnumParticipant interface</span></span>

<span data-ttu-id="29ed4-105">\[**IEnumParticipant** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="29ed4-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="29ed4-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="29ed4-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="29ed4-107">L’interface **IEnumParticipant** fournit des méthodes d’énumération COM standard pour l’interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="29ed4-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="29ed4-108">La méthode [**ITParticipantControl :: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) retourne un pointeur vers **IEnumParticipant**.</span><span class="sxs-lookup"><span data-stu-id="29ed4-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="29ed4-109">L’interface **IEnumParticipant** est masquée dans les langages de script et de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="29ed4-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="29ed4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="29ed4-110">Members</span></span>

<span data-ttu-id="29ed4-111">L’interface **IEnumParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="29ed4-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="29ed4-112">**IEnumParticipant** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29ed4-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="29ed4-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="29ed4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="29ed4-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="29ed4-114">Methods</span></span>

<span data-ttu-id="29ed4-115">L’interface **IEnumParticipant** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="29ed4-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="29ed4-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="29ed4-116">Method</span></span>                                  | <span data-ttu-id="29ed4-117">Description</span><span class="sxs-lookup"><span data-stu-id="29ed4-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29ed4-118">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="29ed4-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="29ed4-119">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="29ed4-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="29ed4-120">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="29ed4-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="29ed4-121">Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="29ed4-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="29ed4-122">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="29ed4-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="29ed4-123">Réinitialise au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="29ed4-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="29ed4-124">**Saut**</span><span class="sxs-lookup"><span data-stu-id="29ed4-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="29ed4-125">Ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="29ed4-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="29ed4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29ed4-126">Requirements</span></span>



| <span data-ttu-id="29ed4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29ed4-127">Requirement</span></span> | <span data-ttu-id="29ed4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="29ed4-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29ed4-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="29ed4-129">TAPI version</span></span><br/> | <span data-ttu-id="29ed4-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="29ed4-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="29ed4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="29ed4-131">Header</span></span><br/>       | <dl> <span data-ttu-id="29ed4-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ed4-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="29ed4-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29ed4-133">Library</span></span><br/>      | <dl> <span data-ttu-id="29ed4-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29ed4-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="29ed4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="29ed4-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="29ed4-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29ed4-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="29ed4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29ed4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ed4-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="29ed4-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

