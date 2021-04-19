---
description: L’interface ITParticipantControl est implémentée par le MSP IPConf.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interface ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537528"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="f28c7-103">Interface ITParticipantControl</span><span class="sxs-lookup"><span data-stu-id="f28c7-103">ITParticipantControl interface</span></span>

<span data-ttu-id="f28c7-104">\[**ITParticipantControl** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f28c7-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f28c7-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f28c7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f28c7-106">L’interface **ITParticipantControl** est implémentée par le MSP ipconf.</span><span class="sxs-lookup"><span data-stu-id="f28c7-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="f28c7-107">Cette interface est exposée sur l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="f28c7-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="f28c7-108">Cette interface permet à une application de récupérer des pointeurs vers les participants d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="f28c7-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="f28c7-109">L’interface **ITParticipantControl** est créée en appelant **QueryInterface** sur [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="f28c7-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="f28c7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f28c7-110">Members</span></span>

<span data-ttu-id="f28c7-111">L’interface **ITParticipantControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f28c7-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f28c7-112">**ITParticipantControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f28c7-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="f28c7-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f28c7-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f28c7-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f28c7-114">Methods</span></span>

<span data-ttu-id="f28c7-115">L’interface **ITParticipantControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f28c7-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="f28c7-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="f28c7-116">Method</span></span>                                                                      | <span data-ttu-id="f28c7-117">Description</span><span class="sxs-lookup"><span data-stu-id="f28c7-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f28c7-118">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="f28c7-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="f28c7-119">Énumère les participants actuellement impliqués dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="f28c7-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="f28c7-120">**accéder aux \_ participants**</span><span class="sxs-lookup"><span data-stu-id="f28c7-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="f28c7-121">Crée une collection de participants associés à la Conférence en cours.</span><span class="sxs-lookup"><span data-stu-id="f28c7-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="f28c7-122">Fourni pour les applications clientes Automation, telles que celles écrites en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f28c7-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f28c7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f28c7-123">Requirements</span></span>



| <span data-ttu-id="f28c7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f28c7-124">Requirement</span></span> | <span data-ttu-id="f28c7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f28c7-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f28c7-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f28c7-126">TAPI version</span></span><br/> | <span data-ttu-id="f28c7-127">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f28c7-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f28c7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f28c7-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f28c7-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="f28c7-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f28c7-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f28c7-130">Library</span></span><br/>      | <dl> <span data-ttu-id="f28c7-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f28c7-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f28c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f28c7-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="f28c7-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f28c7-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

