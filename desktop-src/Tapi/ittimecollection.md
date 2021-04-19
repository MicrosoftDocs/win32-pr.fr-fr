---
description: L’interface ITTimeCollection est une interface propre au fournisseur pour l’objet blob de conférence du protocole SDP (session descripteur).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interface ITTimeCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525424"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="d477e-103">Interface ITTimeCollection</span><span class="sxs-lookup"><span data-stu-id="d477e-103">ITTimeCollection interface</span></span>

<span data-ttu-id="d477e-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d477e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d477e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d477e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d477e-106">L’interface **ITTimeCollection** est une interface propre au fournisseur pour l’objet blob de conférence du protocole SDP (session descripteur).</span><span class="sxs-lookup"><span data-stu-id="d477e-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="d477e-107">Cette interface permet l’accès aux interfaces [**ITTime**](ittime.md) par index, ainsi que la création et la suppression de composants de temps.</span><span class="sxs-lookup"><span data-stu-id="d477e-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="d477e-108">La méthode [**ITSdp :: obten \_ TimeCollection**](itsdp-get-timecollection.md) crée l’interface **ITTimeCollection** .</span><span class="sxs-lookup"><span data-stu-id="d477e-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="d477e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d477e-109">Members</span></span>

<span data-ttu-id="d477e-110">L’interface **ITTimeCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d477e-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d477e-111">**ITTimeCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d477e-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="d477e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d477e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d477e-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d477e-113">Methods</span></span>

<span data-ttu-id="d477e-114">L’interface **ITTimeCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d477e-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="d477e-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="d477e-115">Method</span></span>                                                           | <span data-ttu-id="d477e-116">Description</span><span class="sxs-lookup"><span data-stu-id="d477e-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d477e-117">**Créés**</span><span class="sxs-lookup"><span data-stu-id="d477e-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="d477e-118">Crée un composant [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="d477e-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="d477e-119">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="d477e-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="d477e-120">Supprime un composant [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="d477e-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="d477e-121">**Obtient la \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d477e-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="d477e-122">Retourne un énumérateur pour cette collection.</span><span class="sxs-lookup"><span data-stu-id="d477e-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="d477e-123">**nombre d’extractions \_**</span><span class="sxs-lookup"><span data-stu-id="d477e-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="d477e-124">Obtient le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d477e-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="d477e-125">**Obtient \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="d477e-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="d477e-126">Retourne l’interface d’énumération [**IEnumTime**](ienumtime.md) qui énumère [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="d477e-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="d477e-127">**recevoir un \_ élément**</span><span class="sxs-lookup"><span data-stu-id="d477e-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="d477e-128">Pour un index donné, retourne un élément dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d477e-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="d477e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d477e-129">Requirements</span></span>



| <span data-ttu-id="d477e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d477e-130">Requirement</span></span> | <span data-ttu-id="d477e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d477e-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d477e-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d477e-132">TAPI version</span></span><br/> | <span data-ttu-id="d477e-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d477e-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d477e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="d477e-134">Header</span></span><br/>       | <dl> <span data-ttu-id="d477e-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d477e-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d477e-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d477e-136">Library</span></span><br/>      | <dl> <span data-ttu-id="d477e-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d477e-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d477e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d477e-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="d477e-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d477e-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

