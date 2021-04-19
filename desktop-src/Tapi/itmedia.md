---
description: L’interface ITMedia est une représentation de média dans un protocole SDP (session Description Protocol), consultez RFC 2327.
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interface ITMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526327"
---
# <a name="itmedia-interface"></a><span data-ttu-id="0d16e-103">Interface ITMedia</span><span class="sxs-lookup"><span data-stu-id="0d16e-103">ITMedia interface</span></span>

<span data-ttu-id="0d16e-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0d16e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0d16e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0d16e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0d16e-106">L’interface **ITMedia** est une représentation de média dans un protocole SDP (session Description Protocol), consultez RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="0d16e-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="0d16e-107">Cette interface exporte des méthodes pour récupérer et définir des propriétés de média de base, telles que le type.</span><span class="sxs-lookup"><span data-stu-id="0d16e-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="0d16e-108">Les méthodes [**ITMediaCollection :: obten \_ Item**](itmediacollection-get-item.md) et [**ITMediaCollection :: Create**](itmediacollection-create.md) créent l’interface **ITMedia** .</span><span class="sxs-lookup"><span data-stu-id="0d16e-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="0d16e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0d16e-109">Members</span></span>

<span data-ttu-id="0d16e-110">L’interface **ITMedia** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0d16e-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0d16e-111">**ITMedia** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0d16e-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="0d16e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0d16e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0d16e-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0d16e-113">Methods</span></span>

<span data-ttu-id="0d16e-114">L’interface **ITMedia** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0d16e-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="0d16e-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="0d16e-115">Method</span></span>                                                          | <span data-ttu-id="0d16e-116">Description</span><span class="sxs-lookup"><span data-stu-id="0d16e-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d16e-117">**Obtient \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="0d16e-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="0d16e-118">Obtient la liste des codes de format de charge utile du média.</span><span class="sxs-lookup"><span data-stu-id="0d16e-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="0d16e-119">**recevoir \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="0d16e-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="0d16e-120">Obtient le nom du support.</span><span class="sxs-lookup"><span data-stu-id="0d16e-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="0d16e-121">**Obtient \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="0d16e-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="0d16e-122">Obtient le titre du support.</span><span class="sxs-lookup"><span data-stu-id="0d16e-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="0d16e-123">**Obtient \_ NumPorts**</span><span class="sxs-lookup"><span data-stu-id="0d16e-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="0d16e-124">Obtient le nombre de ports nécessaires pour la session.</span><span class="sxs-lookup"><span data-stu-id="0d16e-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="0d16e-125">**Obtient \_ StartPort**</span><span class="sxs-lookup"><span data-stu-id="0d16e-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="0d16e-126">Obtient la valeur de port 16 bits pour le premier port.</span><span class="sxs-lookup"><span data-stu-id="0d16e-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="0d16e-127">**Obtient \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="0d16e-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="0d16e-128">Obtient le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="0d16e-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="0d16e-129">**put \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="0d16e-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="0d16e-130">Définit la liste des codes de format de charge utile du média.</span><span class="sxs-lookup"><span data-stu-id="0d16e-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="0d16e-131">**put \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="0d16e-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="0d16e-132">Définit le nom du support.</span><span class="sxs-lookup"><span data-stu-id="0d16e-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="0d16e-133">**put \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="0d16e-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="0d16e-134">Définit le titre du support.</span><span class="sxs-lookup"><span data-stu-id="0d16e-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="0d16e-135">**put \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="0d16e-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="0d16e-136">Définit le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="0d16e-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="0d16e-137">**SetPortInfo**</span><span class="sxs-lookup"><span data-stu-id="0d16e-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="0d16e-138">Définit la valeur du port 16 bits pour le premier port et le nombre de ports nécessaires pour la session.</span><span class="sxs-lookup"><span data-stu-id="0d16e-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d16e-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d16e-139">Requirements</span></span>



| <span data-ttu-id="0d16e-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d16e-140">Requirement</span></span> | <span data-ttu-id="0d16e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d16e-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d16e-142">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0d16e-142">TAPI version</span></span><br/> | <span data-ttu-id="0d16e-143">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0d16e-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0d16e-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d16e-144">Header</span></span><br/>       | <dl> <span data-ttu-id="0d16e-145"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d16e-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d16e-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d16e-146">Library</span></span><br/>      | <dl> <span data-ttu-id="0d16e-147"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d16e-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0d16e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0d16e-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="0d16e-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d16e-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d16e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d16e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d16e-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0d16e-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="0d16e-152">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="0d16e-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="0d16e-153">**ITSDP**</span><span class="sxs-lookup"><span data-stu-id="0d16e-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="0d16e-154">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="0d16e-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

