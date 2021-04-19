---
description: L’interface ITTime est une interface propre au fournisseur pour un objet blob de conférence SDP (session Descriptor Protocol).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interface ITTime (sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542301"
---
# <a name="ittime-interface"></a><span data-ttu-id="6a986-103">Interface ITTime</span><span class="sxs-lookup"><span data-stu-id="6a986-103">ITTime interface</span></span>

<span data-ttu-id="6a986-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6a986-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a986-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6a986-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6a986-106">L’interface **ITTime** est une interface propre au fournisseur pour un objet blob de conférence SDP (session Descriptor Protocol).</span><span class="sxs-lookup"><span data-stu-id="6a986-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="6a986-107">Il permet d’accéder à un ensemble de temps d’activation pour la session.</span><span class="sxs-lookup"><span data-stu-id="6a986-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="6a986-108">Les méthodes [**IEnumTime :: Next**](ienumtime-next.md) et [**ITTimeCollection :: Create**](ittimecollection-create.md) créent l’interface **ITTime** .</span><span class="sxs-lookup"><span data-stu-id="6a986-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="6a986-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6a986-109">Members</span></span>

<span data-ttu-id="6a986-110">L’interface **ITTime** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6a986-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6a986-111">**ITTime** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a986-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="6a986-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6a986-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a986-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6a986-113">Methods</span></span>

<span data-ttu-id="6a986-114">L’interface **ITTime** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6a986-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="6a986-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="6a986-115">Method</span></span>                                         | <span data-ttu-id="6a986-116">Description</span><span class="sxs-lookup"><span data-stu-id="6a986-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="6a986-117">**Obtient \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="6a986-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="6a986-118">Obtient la valeur d’heure de début NTP (Network Time Protocol) 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a986-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="6a986-119">**Obtient \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="6a986-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="6a986-120">Obtient la valeur de l’heure de fin NTP.</span><span class="sxs-lookup"><span data-stu-id="6a986-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="6a986-121">**put \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="6a986-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="6a986-122">Définit la valeur d’heure de début NTP 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a986-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="6a986-123">**put \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="6a986-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="6a986-124">Définit la valeur de l’heure de fin NTP.</span><span class="sxs-lookup"><span data-stu-id="6a986-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="6a986-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a986-125">Requirements</span></span>



| <span data-ttu-id="6a986-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a986-126">Requirement</span></span> | <span data-ttu-id="6a986-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a986-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a986-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6a986-128">TAPI version</span></span><br/> | <span data-ttu-id="6a986-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6a986-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6a986-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a986-130">Header</span></span><br/>       | <dl> <span data-ttu-id="6a986-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a986-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a986-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a986-132">Library</span></span><br/>      | <dl> <span data-ttu-id="6a986-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a986-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6a986-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6a986-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="6a986-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a986-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

