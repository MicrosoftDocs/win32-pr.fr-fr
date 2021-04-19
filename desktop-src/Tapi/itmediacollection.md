---
description: L’interface ITMediaCollection fournit l’accès à l’ensemble d’informations de média dans une description de conférence SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interface ITMediaCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540973"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="033e4-103">Interface ITMediaCollection</span><span class="sxs-lookup"><span data-stu-id="033e4-103">ITMediaCollection interface</span></span>

<span data-ttu-id="033e4-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="033e4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="033e4-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="033e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="033e4-106">L’interface **ITMediaCollection** fournit l’accès à l’ensemble d’informations de média dans une description de conférence SDP (RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="033e4-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="033e4-107">Chaque description de support dans le SDP est décrite par une interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="033e4-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="033e4-108">**ITMediaCollection** permet de manipuler le jeu d’informations de **ITMEDIA** pour le SDP, y compris :</span><span class="sxs-lookup"><span data-stu-id="033e4-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="033e4-109">Autorise l’accès aux médias par index.</span><span class="sxs-lookup"><span data-stu-id="033e4-109">Allows media access by index.</span></span>
-   <span data-ttu-id="033e4-110">Permet la création et la suppression de médias.</span><span class="sxs-lookup"><span data-stu-id="033e4-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="033e4-111">La méthode [**ITSdp :: obten \_ MediaCollection**](itsdp-get-mediacollection.md) crée l’interface **ITMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="033e4-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="033e4-112">Membres</span><span class="sxs-lookup"><span data-stu-id="033e4-112">Members</span></span>

<span data-ttu-id="033e4-113">L’interface **ITMediaCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="033e4-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="033e4-114">**ITMediaCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="033e4-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="033e4-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="033e4-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="033e4-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="033e4-116">Methods</span></span>

<span data-ttu-id="033e4-117">L’interface **ITMediaCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="033e4-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="033e4-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="033e4-118">Method</span></span>                                                            | <span data-ttu-id="033e4-119">Description</span><span class="sxs-lookup"><span data-stu-id="033e4-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="033e4-120">**Créés**</span><span class="sxs-lookup"><span data-stu-id="033e4-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="033e4-121">Crée un nouveau média avec les propriétés par défaut et le retourne.</span><span class="sxs-lookup"><span data-stu-id="033e4-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="033e4-122">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="033e4-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="033e4-123">Supprime le support correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="033e4-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="033e4-124">**Obtient la \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="033e4-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="033e4-125">Retourne un énumérateur pour cette collection.</span><span class="sxs-lookup"><span data-stu-id="033e4-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="033e4-126">**nombre d’extractions \_**</span><span class="sxs-lookup"><span data-stu-id="033e4-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="033e4-127">Obtient le nombre de médias dans la session.</span><span class="sxs-lookup"><span data-stu-id="033e4-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="033e4-128">**Obtient \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="033e4-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="033e4-129">Obtient un pointeur vers l’interface d’énumération.</span><span class="sxs-lookup"><span data-stu-id="033e4-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="033e4-130">**recevoir un \_ élément**</span><span class="sxs-lookup"><span data-stu-id="033e4-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="033e4-131">Retourne le média correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="033e4-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="033e4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="033e4-132">Requirements</span></span>



| <span data-ttu-id="033e4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="033e4-133">Requirement</span></span> | <span data-ttu-id="033e4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="033e4-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="033e4-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="033e4-135">TAPI version</span></span><br/> | <span data-ttu-id="033e4-136">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="033e4-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="033e4-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="033e4-137">Header</span></span><br/>       | <dl> <span data-ttu-id="033e4-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="033e4-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="033e4-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="033e4-139">Library</span></span><br/>      | <dl> <span data-ttu-id="033e4-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="033e4-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="033e4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="033e4-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="033e4-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="033e4-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

