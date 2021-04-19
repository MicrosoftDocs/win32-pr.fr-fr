---
description: L’interface ITLocalParticipant est exposée sur l’objet de flux lorsque le MSP IPConf prend en charge l’appel.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interface ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537781"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="7c2de-103">Interface ITLocalParticipant</span><span class="sxs-lookup"><span data-stu-id="7c2de-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="7c2de-104">L’interface **ITLocalParticipant** est exposée sur l’objet de flux lorsque le MSP ipconf prend en charge l’appel.</span><span class="sxs-lookup"><span data-stu-id="7c2de-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="7c2de-105">Le MSP implémente des méthodes qui permettent à une application d’accéder à des informations sur les participants et de les définir.</span><span class="sxs-lookup"><span data-stu-id="7c2de-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="7c2de-106">L’interface **ITLocalParticipant** est créée en appelant **QueryInterface** sur [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="7c2de-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="7c2de-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7c2de-107">Members</span></span>

<span data-ttu-id="7c2de-108">L’interface **ITLocalParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7c2de-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7c2de-109">**ITLocalParticipant** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c2de-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="7c2de-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7c2de-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c2de-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7c2de-111">Methods</span></span>

<span data-ttu-id="7c2de-112">L’interface **ITLocalParticipant** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7c2de-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="7c2de-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="7c2de-113">Method</span></span>                                                                                     | <span data-ttu-id="7c2de-114">Description</span><span class="sxs-lookup"><span data-stu-id="7c2de-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c2de-115">**Obtient \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="7c2de-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="7c2de-116">Obtient des informations sur les participants, telles que le nom du courrier électronique ou l’emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="7c2de-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="7c2de-117">**put \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="7c2de-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="7c2de-118">Définit les informations sur le participant.</span><span class="sxs-lookup"><span data-stu-id="7c2de-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="7c2de-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c2de-119">Requirements</span></span>



| <span data-ttu-id="7c2de-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c2de-120">Requirement</span></span> | <span data-ttu-id="7c2de-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c2de-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2de-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7c2de-122">TAPI version</span></span><br/> | <span data-ttu-id="7c2de-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7c2de-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7c2de-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c2de-124">Header</span></span><br/>       | <dl> <span data-ttu-id="7c2de-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2de-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7c2de-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c2de-126">Library</span></span><br/>      | <dl> <span data-ttu-id="7c2de-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c2de-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7c2de-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7c2de-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="7c2de-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c2de-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7c2de-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c2de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2de-131">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="7c2de-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

